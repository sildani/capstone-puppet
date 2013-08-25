# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "capstone"
  config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-59-x64-vbox4210.box"
  config.vm.hostname = "daniel.puppetlabs.vm"
  config.vm.network :private_network, ip: "192.168.33.10"
  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "vagrant/manifests"
    puppet.manifest_file  = "init.pp"
  end
end
