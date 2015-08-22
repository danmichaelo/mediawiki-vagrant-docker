# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  config.vm.network "private_network", ip: "192.168.33.159"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end
  config.vm.provision "docker" do |d|
    d.build_image "/vagrant/1.24", args: "-t danmichaelo/mediawiki:1.24"
    d.run "mediawiki-1", image: "danmichaelo/mediawiki:1.24", args: "-p 80:80"
  end
end
