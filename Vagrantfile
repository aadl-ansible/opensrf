# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.define "opensrf-test"
  config.vm.hostname = "opensrf-test"
  config.vm.provider "virtualbox" do |vb|
     vb.name = "opensrf-test-box"
  end
  config.vm.network "private_network", ip: "192.168.10.10"
  config.vm.provision "shell", inline: <<-SHELL
    echo -e "testingpass\ntestingpass" | passwd ubuntu
  SHELL
end
