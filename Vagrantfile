# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

$script = <<SCRIPT
export GOPATH=/home/vagrant/gocode
mkdir -p /home/vagrant/gocode/src/github.com/hashicorp
SCRIPT

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "jess/ubuntu-go"

  config.vm.synced_folder ".", "/home/vagrant/gocode/src/github.com/hashicorp/serf"
  config.vm.network "forwarded_port", guest: 7946, host: 7946
  config.vm.network "forwarded_port", guest: 7373, host: 7373
end
