# -*- mode: ruby -*-
# vi: set ft=ruby :

# Definitions of the VMs.
boxes = [
    { 'hostname' => 'ansible-box', 'ip' => '192.168.56.99' }
]

Vagrant.configure("2") do |config|
    boxes.each do |box|
        config.vm.define box['hostname'] do |instance|
            instance.vm.box = "bento/ubuntu-21.10"
            instance.vm.box_version = "202112.19.0"

            instance.vm.hostname = box['hostname']
            instance.vm.network :private_network, ip: box['ip']

            instance.vm.provider "virtualbox" do |vb|
                vb.memory = "1024"
            end
        end
    end

    config.vm.provision "ansible" do |ansible|
       ansible.playbook = "provision_vagrant.yml"
    end
end
