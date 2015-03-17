# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu/trusty64"

  # Create a slightly more powerful default virtual machine
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end
  config.berkshelf.enabled = true
  config.berkshelf.berksfile_path = "ops/config/Berksfile"

  # Basic provisioning
  config.vm.provision "chef_zero" do |chef|
    chef.cookbooks_path = "ops/config"
    chef.roles_path = "ops/dna/roles"

    chef.add_role "core"
  end
  
  # Use docker container for local database
  config.vm.provision "docker", run: "always" do |d|
    d.pull_images 'postgres'
    d.run 'postgres:9.3', args: "-e POSTGRES_PASSWORD=postgres -e POSTGRES_USER=postgres -d --name postgres -p 5432:5432"
  end

  # Forward ports   
  config.vm.network "forwarded_port", guest: 5432, host: 5432   #postgres
  

  
end