Vagrant.configure(2) do |mylab|
    mylab.vm.define "atomic1" do | atm1 |
        atm1.vm.box = "fedora/24-atomic-host"
        atm1.vm.provider :libvirt do |domain|
            domain.memory = 2048
            domain.driver = "qemu"
            domain.vm.network :hostonly, "192.168.33.10"
        end
    end
end
