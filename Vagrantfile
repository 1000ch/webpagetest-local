# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "chef/centos-6.5"
  config.vm.hostname = "webpagetest-local"

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :private_network, ip: "192.168.33.10"

  config.vm.synced_folder "../webpagetest/www", "/var/www/webpagetest"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "webpagetest-local.yml"
    ansible.inventory_path = "hosts"
    ansible.limit = "all"
    ansible.verbose = "v"
  end

end
