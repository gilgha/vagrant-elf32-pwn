# vagrant-elf32-pwn
Simple vagrant project to rapidly spin up a Ubuntu 16.04 x86 virtual machine which already includes the tools required to pwn ELF32 binaries.

## Requirements
You will need the following software to use this project:

| Software 			| Download Link 							|
| ----------------- | ----------------------------------------- |
| Vagrant 			| https://www.vagrantup.com/downloads.html 	|
| Oracle VirtualBox | https://www.virtualbox.org/wiki/Downloads |

## Usage
To start the virtual machine, use the following command from the root project directory:

    $ vagrant up

Then use the following command to get to the virtual machine Bash shell:

    $ vagrant ssh

If you are running **Windows**, consider using the `vagrant-multi-putty` plugin instead:
https://github.com/nickryand/vagrant-multi-putty

The `workdir` directory is used to share files between your host and the virtual machine.

| Context 	| Path 						|
| --------- | ------------------------- |
| Host 		| \<PROJECT ROOT\>/workdir 	|
| VM 		| /vagrant/workdir 			|

Please do not write into the project root to avoid messing with Git. 

Finally, suspend, halt or destroy your Vagrant virtual machine:

    $ vagrant suspend
    $ vagrant halt
    $ vagrant destroy
