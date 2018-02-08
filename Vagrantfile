# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "elf32-pwn"

  config.vm.box = "ubuntu/xenial32"
  config.vm.hostname = "elf32-pwn"

  config.vm.provision "shell", path: "provision/apt-update.sh", privileged: true
  config.vm.provision "shell", path: "provision/install-tools.sh", privileged: true
  config.vm.provision "shell", path: "provision/install-radare2.sh", privileged: true
  config.vm.provision "shell", path: "provision/setup-bashrc.sh", privileged: false

  config.vm.post_up_message = "Done! You can now start pwning in this ELF32 environment :-) !"
end
