# -*- mode: ruby -*-
# vi: set ft=ruby :

ANSIBLE_GROUPS = {"vagrant" => ["default"]}

Vagrant.configure(2) do |config|
  #Vagrant Box https://atlas.hashicorp.com/boxes/search
  config.vm.box = "box-cutter/ubuntu1404-desktop"
  config.cache.scope = :box if Vagrant.has_plugin?("vagrant-cachier")

  #Hardware Specifications
  config.vm.provider "virtualbox" do |v|
    v.name = "DataToolsBoxUbuntuDesktop"
    v.memory = 2048
    v.cpus = 2
  end

  #Code to provision the box
  config.vm.provision "ansible" do |ansible|
    ansible.groups = ANSIBLE_GROUPS
    ansible.playbook = "playbook.yml"
  end
end
