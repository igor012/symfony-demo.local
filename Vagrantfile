# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "db" do |db|
    db.vm.box = "debian/contrib-buster64"
    db.vm.box_version = "10.1.0"
    db.vm.hostname="db"
    db.vm.network :private_network, ip: "10.0.15.20"
  end

  config.vm.define "web" do |web|
    web.vm.box = "debian/contrib-buster64"
    web.vm.box_version = "10.1.0"
    web.vm.hostname="web"
    web.vm.network :private_network, ip: "10.0.15.10"
    web.vm.network "forwarded_port", guest: 80, host: 8080
    web.vm.synced_folder "code/project", "/var/www/project", owner: "www-data", group: "www-data"
  end


  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yaml"
  end
end