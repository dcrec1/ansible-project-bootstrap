# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  box = ENV['VAGRANT_BOX'] || "precise32"
  config.vm.box = box
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.provision "ansible" do |ansible|
    ansible.limit = 'all'
    ansible.inventory_path = "inventory/development"
    ansible.playbook = "#{ENV['PLAYBOOK']}.yml"
  end
  config.ssh.forward_agent = true
end
