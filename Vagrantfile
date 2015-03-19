# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "fillup/centos-6.5-i386-minimal"
  config.vm.network "forwarded_port", guest: 8080, host: 8000
  config.vm.define "jenkins" do |jenkins|
  end
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "1024"
     vb.cpus = 1
     vb.name = "jenkins"
  end
end
