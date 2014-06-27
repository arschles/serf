# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "jess/ubuntu-go"

  config.vm.provision "shell", inline: "mkdir -p /home/vagrant/go"
  config.vm.provision "shell", inline: "chown -R vagrant /home/vagrant/go"
  config.vm.provision "shell", inline: "chmod -R u+rwx /home/vagrant/go"
  config.vm.synced_folder ".", "/home/vagrant/go/src/github.com/hashicorp/serf"
  config.vm.network "forwarded_port", guest: 7946, host: 7946
  config.vm.network "forwarded_port", guest: 7373, host: 7373
end
