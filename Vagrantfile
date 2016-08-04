# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    #config.vm.box = "akasurde/fedora-24-x86_64"
    config.vm.box = "bento/fedora-24"
    config.vm.synced_folder ".", "/vagrant", disabled: true
    #config.vm.provider :libvirt do |libvirt|
    #    libvirt.driver = "qemu"
    #    libvirt.memory = 1024
        #libvirt.management_network_name = 'vagrant-libvirt-new'
        #libvirt.management_network_address = '192.168.124.0/24'
    #end
    config.vm.provider "virtualbox"
    config.vm.provision "shell",
      inline: "hostname --fqdn > /etc/hostname && hostname -F /etc/hostname"
    config.vm.provision "shell",
      inline: "hostname --fqdn > /etc/hostname && hostname -F /etc/hostname"
    config.vm.define "server" do |server|
       server.vm.network "private_network", ip: "192.168.33.10"
    end
    #config.vm.provision :shell, path: "bootstrap.sh"
end
