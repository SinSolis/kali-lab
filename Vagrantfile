# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  os = "kalilinux/rolling"
  net_ip = "192.168.50"

  config.vm.define :kali, primary: true do |kali_config|
    kali_config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = 2
        vb.name = "kali"
        vb.gui = false
    end
    kali_config.vm.box = "#{os}"
    kali_config.vm.host_name = 'kali.local'
    kali_config.vm.network "private_network", ip: "#{net_ip}.23"
    kali_config.vm.network "public_network", bridge: "Intel(R) Wi-Fi 6 AX201 160MHz"
    end
end