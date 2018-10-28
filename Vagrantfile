# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"
  # config.vm.box = "ubuntu/xenial64"
  # config.vm.box_version = "20181024.0.0"

  # config.vm.box = "centos/7"
  # config.vm.box_version = "1809.01"

  # config.vm.box_check_update = false

  config.vm.network "forwarded_port", guest: 2181, host: 2181
  config.vm.network "forwarded_port", guest: 9092, host: 9092
  config.vm.network "forwarded_port", guest: 8091, host: 8091
  config.vm.network "forwarded_port", guest: 9200, host: 9200
  # Following is for 2nd & 3rd node in Kafka cluster
  # config.vm.network "forwarded_port", guest: 9093, host: 9093
  # config.vm.network "forwarded_port", guest: 9094, host: 9094

  config.vm.network "private_network", ip: "192.168.32.10"

  config.vm.post_up_message = "The dev infra is up!"

  config.vm.provider "virtualbox" do |vb|
    # vb.gui = true
    vb.name = "infra_on_ubuntu"
    vb.memory = "4096"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end