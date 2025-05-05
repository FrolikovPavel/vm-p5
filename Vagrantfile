# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  
  (1..2).each do |i|
    config.vm.define "ansible-vm#{i}" do |vm|    
      vm.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "playbook.yml"
      end
    end
  end
end
