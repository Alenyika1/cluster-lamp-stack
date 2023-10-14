# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile for Master and Slave nodes with LAMP Stack

Vagrant.configure("2") do |config|
  # Configuration for the Master node
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/focal64"
    master.vm.hostname = "master"
    master.vm.network "private_network", ip: "192.168.56.5"
    
    # # Copy the SSH public key from your local machine to the "master" VM
    # config.vm.provision "file", source: "C:\\Users\\USER\\.ssh\\id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"
    
    # Share an additional folder to the guest VM.
    config.vm.synced_folder ".", "/vagrant"
  end

  # Configuration for the Slave node
  config.vm.define "slave" do |slave|
    slave.vm.box = "ubuntu/focal64"
    slave.vm.hostname = "slave"
    slave.vm.network "private_network", ip: "192.168.56.6"
  end
end
