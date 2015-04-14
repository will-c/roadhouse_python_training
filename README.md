# data-training-module
Data, code, and configurations for the AIT Data/SQL/Python training module


## Setup Instructions
#### Programs
0. Install Virtualbox: https://www.virtualbox.org/wiki/Downloads
0. Install Vagrant: https://www.vagrantup.com/downloads.html
0. Install Git
#### Project Workspace Setup
0. Create a new parent folder for projects of this type at the root of your C: drive. (e.g.: C:\projects)
0. Open a command prompt and navigate into the folder you just created
	* Windows key + R, then enter `cmd` in the box and click OK.
	* Type `cd c:\projects` (or whatever you named it) and press Return.
0. Clone the project repository




## Summary of current version contents
* PostgreSQL Client 9.3
* Docker Container running PostgreSQL server
* Port 5432 passed through from the guest to the container
* Port 5432 on guest exposed on host as 5434