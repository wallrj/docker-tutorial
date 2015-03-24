# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

$bootstrap = <<SCRIPT
set -e

# Pre-cache some Docker images here too in case user has an older base box.
docker pull ubuntu:14.04
docker pull tutum/apache-php
SCRIPT

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "wallrj/docker-tutorial-environment"
  config.vm.network :private_network, :ip => "172.16.255.250"
  config.vm.hostname = "docker-tutorial"
  config.vm.provision :shell, :inline => $bootstrap, :privileged => true
end
