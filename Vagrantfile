# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  
  #nombre del box
  config.vm.box = "debian"

  #configuraciones de red
  config.vm.network "forwarded_port", guest: 80, host: 8080 
  config.vm.network "private_network", ip: "192.168.33.10"

  #proveedor de virtualizacion
  config.vm.provider "virtualbox" do |vb|
  
  #memoria virtual  
  vb.memory = "1024"
  end
 
  #playbook que debe ejecutarse
  config.vm.provision "ansible" do |ansible|
  ansible.playbook = "tasks/main.yml"
end  
  
end
