# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "akasurde/fedora-24-x86_64"
    config.vm.synced_folder ".", "/vagrant", disabled: true
    #config.vm.provider :libvirt do |libvirt|
    #    libvirt.driver = "qemu"
    #    libvirt.memory = 1024
    #end
    config.vm.provider "virtualbox"
    config.vm.provision "shell",
      inline: "hostname --fqdn > /etc/hostname && hostname -F /etc/hostname"
    config.vm.provision "shell",
      inline: "hostname --fqdn > /etc/hostname && hostname -F /etc/hostname"
    config.vm.define "server" do |server|
       server.vm.network "private_network", ip: "192.168.33.10"
       server.vm.hostname = "server.local"
    end
    #config.vm.provision :shell, path: "bootstrap.sh"
end
