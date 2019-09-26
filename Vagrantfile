# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.define "opensrfapp1" do |opensrfapp1|
    opensrfapp1.vm.network "private_network", ip: "192.168.10.10"
    opensrfapp1.vm.network "forwarded_port", guest: 22, host: 3000, id: 'ssh'
    opensrfapp1.vm.hostname = "opensrfapp1"
    opensrfapp1.vm.provider "virtualbox" do |v|
      v.name = "opensrfapp1"
    end
    opensrfapp1.vm.provision "shell", inline: <<-SHELL
      echo -e "testingpass\ntestingpass" | passwd ubuntu
    SHELL
  end
  config.vm.define "opensrfapp2" do |opensrfapp2|
    opensrfapp2.vm.network "private_network", ip: "192.168.10.11"
    opensrfapp2.vm.network "forwarded_port", guest: 22, host: 3001, id: 'ssh'
    opensrfapp2.vm.hostname = "opensrfapp2"
    opensrfapp2.vm.provider "virtualbox" do |v|
      v.name = "opensrfapp2"
    end
    opensrfapp2.vm.provision "shell", inline: <<-SHELL
      echo -e "testingpass\ntestingpass" | passwd ubuntu
    SHELL
  end
  config.vm.define "opensrfapp3" do |opensrfapp3|
    opensrfapp3.vm.network "private_network", ip: "192.168.10.12"
    opensrfapp3.vm.network "forwarded_port", guest: 22, host: 3002, id: 'ssh'
    opensrfapp3.vm.hostname = "opensrfapp3"
    opensrfapp3.vm.provider "virtualbox" do |v|
      v.name = "opensrfapp3"
    end
    opensrfapp3.vm.provision "shell", inline: <<-SHELL
      echo -e "testingpass\ntestingpass" | passwd ubuntu
    SHELL
  end
end
