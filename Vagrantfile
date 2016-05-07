# -*- mode: ruby -*-
# vi: set ft=ruby :
#
# Author: Zak Hassan
#

  Vagrant.configure(2) do |config|
    config.vm.box = "bento/centos-7.1"
    config.vm.provider "virtualbox" do |v|
        v.memory = 1024
      end
    config.vm.define "standalone" do |d|
         d.vm.provision :shell, path: "bootstrap_monitord.sh"
         d.vm.hostname = "monitord.bzcareer.com"
         d.vm.network "private_network", ip: "192.168.33.10"
    end
end
