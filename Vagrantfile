# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "bento/fedora-24"
    config.vm.synced_folder ".", "/vagrant", disabled: true
    config.vm.provider "virtualbox"
    config.vm.box_check_update = false

    config.vm.provision "shell",
        inline: "sed -ri 's/127\.0\.0\.1\s.*/127.0.0.1 localhost localhost.localdomain/' /etc/hosts"

    config.vm.define "server" do |server|
       server.vm.network "private_network", ip: "192.168.33.10"
       server.vm.hostname = "server.localdomain"
       #server.vm.provision "shell",
       #  inline: "mkdir test && echo 'escribiendo en archivo' > test/file.txt && cat test/file.txt"
    end
end
