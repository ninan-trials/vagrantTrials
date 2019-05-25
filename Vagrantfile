# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define :puppetmaster do |puppet_master_config|
    puppet_master_config.vm.box = "ubuntu/trusty64"
    puppet_master_config.vm.network :private_network, ip: "10.0.0.25"
    puppet_master_config.vm.network "forwarded_port", guest: 80, host: 8000
  end
  config.vm.define :puppetclient do |puppet_client_config|
    puppet_client_config.vm.box = "ubuntu/trusty64"
    puppet_client_config.vm.network :private_network, ip: "10.0.0.35"
    puppet_client_config.vm.network "forwarded_port", guest: 80, host: 9001
  end
end

