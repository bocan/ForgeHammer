# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "thor.local"
  config.vm.box = "ubuntu-18.10"  
  config.vm.network "private_network", ip: "172.28.128.10"

#  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 8192
    vb.cpus = 2
    vb.name = "thor.local"
    vb.customize ["modifyvm", :id, "--vram", "128"]

  end

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apt-transport-https ansible docker.io
    swapoff -a
  SHELL

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
  end

end
