# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "base"
  config.vm.box_url = "http://developer.nrel.gov/downloads/vagrant-boxes/CentOS-6.4-x86_64-v20130427.box"

  config.vm.hostname = "webpagetest-local"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :private_network, ip: "192.168.33.10"

  config.vm.synced_folder "../webpagetest/www", "/var/www/webpagetest"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "./webpagetest-local.yml"
    ansible.inventory_path = "hosts"
    ansible.verbose = "v"
  end

end
