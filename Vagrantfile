# -*- mode: ruby -*-
# vi: set ft=ruby :

ANSIBLE_GROUPS = {"vagrant" => ["default"]}

Vagrant.configure(2) do |config|
  #config.vm.box = "Microsoft/EdgeOnWindows10"
  config.vm.box = "chenhan/ubuntu-desktop-18.04"
  config.cache.scope = :box if Vagrant.has_plugin?("vagrant-cachier")

  #Hardware Specifications
  config.vm.provider "virtualbox" do |v|
    v.name = "Curso_DWH_BI_Workstation"
    v.memory = 4096
    v.cpus = 2
  end

  #Code to provision the box
  config.vm.provision "ansible" do |ansible|
    ansible.groups = ANSIBLE_GROUPS
    ansible.playbook = "playbook.yml"
  end
end
