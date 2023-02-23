# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/focal64"
  config.vm.hostname = "vagrant-kind-01"
  config.vm.define  "vagrant-kind-01"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder "./", "/home/vagrant/project"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 4
    vb.memory = "4096"
  end

  config.vm.provision "shell", path: "script.sh"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install dpkg -y
  SHELL

end
  