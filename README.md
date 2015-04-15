# data-training-module
Data, code, and configurations for the AIT Data/SQL/Python training module


## Setup Instructions
#### Prerequisites
0. Install Virtualbox: https://www.virtualbox.org/wiki/Downloads
0. Install Vagrant: https://www.vagrantup.com/downloads.html
0. Install Git: http://git-scm.com/downloads   Choose the following options during the installation wizard:
	* On the first step, check the last box for *use TrueType font in all console windows*
	* On the step titled *Adjusting your PATH environment* choose the second option: *Use Git from the Windows Command Prompt*
	* For all other steps, the default settings are appropriate. 
0. Restart your computer after installing all the prerequisites.

#### Project Workspace Setup
0. Create a new parent folder for projects of this type at the root of your C: drive. (e.g.: C:\projects)
0. Open a command prompt and navigate into the folder you just created
	* Windows key + R, then enter `cmd` in the box and click OK.
	* Type `cd c:\projects` (or whatever you named it) and press Return.
0. Clone the project repository: `git checkout https://github.com/AVCo/data-training-module`

#### Start Vagrant
0. `cd c:\projects\data-training` to change the working directory of your command prompt to the root of the data-training project
0. `vagrant up`. This will start the provisioning process for the virtual machine that will be used for this project. The first time you do this it will do some stuff...

- Add data where the thing can get to it

- Connect putty to test

- Create tunnel in putty

- Connect pgadmin via tunnel





#### Summary of current version contents
* PostgreSQL Client 9.3
* Docker Container running PostgreSQL server
* Port 5432 passed through from the guest to the container
* Port 5432 on guest exposed on host as 5434