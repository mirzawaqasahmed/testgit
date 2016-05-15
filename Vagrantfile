# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|

  config.vm.box = "trusty64"
  config.vm.synced_folder '.', '/vagrant'

  config.vm.define "testgit" do |testgit|
    testgit.vm.host_name = "testgit"
    testgit.vm.network "private_network", type: "dhcp"
    testgit.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y python-pip python-dev git delorean tox
    SHELL
  end
end