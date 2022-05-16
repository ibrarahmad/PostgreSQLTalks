

## PostgreSQL Read Write Scalability

Read Write Scalability

*Author: Ibrar Ahmed*

*Date: 16-May-2022*

*Duration: 3 Hours*

*Video: *

### Abstract

PostgreSQL is one of the leading open-source databases. Out of the box, the default PostgreSQL configuration is not tuned for any particular workload. Nowadays, production systems have quite expensive machines, which require extra configuration. PostgreSQL provides configuration parameters to configure it accordingly. Most of the time, people configure PostgreSQL according to hardware and don’t consider the workload and type of queries. In all these three cases, there’s a different set of configurations. In this talk, users will see how to configure PostgreSQL for a Read/Write intensive load. This talk will explain every important configuration parameter with real-time examples.


### Prerequisite

- Any host OS (Linux, Windows, MacOS)

- PostgreSQL 


Any host OS (Linux, Windows, MacOS) that supports following virtualisation and automation workflow software. 

### Vagrant 

- Vagrant is a tool by HashiCorp for building and managing virtual environment in a single workflow. 
- Supported on MacOS, Linux and Windows. 
- A single declarative configuration file (Vagrantfile) to describe OS, Packages and configuration. We will create and edit this file as per out need. 
- Using Vagrant CLI (command line) and Vagrantfile, we will spawn a VM using Virtualisation provided by VirtualBox. 
- We will install Vagrant latest version 2.2.x, steps in upcoming slides. 

### VirtualBox

- Oracle VM VirtualBox is a hypervisor for x86 virtualization developed by Oracle Corporation. 
- An inception of a computer, where you can run sandboxed OS within your computer. 
- We will use the latest compatible version of VirtualBox 6.1.x to work seamlessly with vagrant.  
- Open your web browser and navigate to https://www.virtualbox.org/wiki/Downloads. 
- Look for heading/caption(VirtualBox 6.1.34 platform packages). 
- Under the above heading, you will find the links for downloading the VirtualBox software for Windows hosts, OX X hosts and Linux distributions. 
- Download the appropriate software distribution as per your computer/laptop OS. 
- Note: In the case of Linux distributions, it will take you to the next page to choose the download package as per your computer’s Linux host flavour. 
- Run the downloaded installer/package and follow the instruction as you proceed.

### Vagrant

- The latest version is 2.2.19 which we need to install. 
- Open your web browser and navigate to https://www.vagrantup.com/downloads. 
- Look for tabs that are specific to your computer OS: macOS, Windows, Linux, Debian 
- For macOS: better to download the macOS binary file and install it, if you are not already using brew, takes time set up to brew itself.  
- For Windows: choose Amd64 (64-bit installer), you are likely to have this architecture. 
- For Linux:  under the Linux, tab chooses the flavour of your OS, and follow the steps. 
- Note: In the case of Linux distributions, it will take you to the next page to choose the download package as per your computer’s Linux host flavour. 
- Run the downloaded installer/package and follow the instructions as you proceed. 

### Ubuntu 

- Download the Ubuntu 20.04.x Vagrant box from Vagrant Cloud to your local machine so that it is accessible to Vagrant CLI and VirtualBox. 
- We will use the ubuntu/focal64 vagrant box from Vagrant Cloud. 
- Run this command to download: vagrant box add ubuntu/focal64 
- After a few moments, the output will let you know it's successful.
- Create a directory where your virutal hosts(s) will live. This will contain all your virtual machines installations and files. 

```

$ mkdir ~/demo 
$ cd demo
$ mkdir ubuntu 
$ cd ubuntu 

```

- Now we need to initiliaze the Ubuntu 20.04.x VM in directory (~/demo/ubuntu), that was created in last step. 
- Run command to initialize and create a Vagrantfile: 

```

$ vagrant init ubuntu/focal64 

```

- Following message will be shown after successfully creating a Vagrantfile in current directory.  A `Vagrantfile` has been placed in this directory. You are now ready to `vagrant up` your first virtual environment! Please read the comments in the Vagrantfile as well as documentation on`vagrantup.com` for more information on using Vagrant. 
- Now we are ready to start up the VM using this command while remaining in same directory: 

```
$ vagrant up
```

- This will create the VM, perform the required configuration, download packages and updates to the VM. 
- After a few minutes, everything is good to go!.
- Login vagrant

```
vagrant ssh
```

### PostgreSQL 14

- Using Ubuntu VM CLI Perform following commands to install the Postgres 14.3 server: 

```bash

$ sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
$ wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
$ sudo apt-get update
$ sudo apt-get -y install postgresql-14
```

- If everything goes as planned, now you are ready to use PostgreSQL server 14.3: 
- Verify installation is successful: 

```
$ sudo psql –V 
psql (PostgreSQL) 14.3 (Ubuntu 14.3-1.pgdg20.04+1)

```

- Edit the postgresql.conf file, use the following command with the file path provided below:$ sudo vim /etc/postgresql/14/main/postgresql.confTo access - Postgres server psql command prompt: 

```
$ sudo -u postgres psql
```

To start/stop/restart Postgres server: 

```
$ sudo service postgresql start
$ sudo service postgresql stop
$ sudo service postgresql restart

```



## Deep Dive To PostgreSQL Indexes

Author: Ibrar Ahmed

Date: 18-May-2022

Duration: 50 Minuts

## PostgreSQL And Artifical Intelegence

Author: Ibrar Ahmed

Date: 18-May-2022

Duration: 50 Minuts
