#!/usr/bin/env ruby
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "querycasts-lab-0.0.1"
  config.vm.box_url =
    "http://assets.querycasts.com/lab/vms/querycasts-lab-0.0.1.box"
  config.vm.host_name = "lab"
  config.vm.network :private_network, "192.168.33.10"
  config.vm.synced_folder ".", "/vagrant", nfs:
      RUBY_PLATFORM =~ /darwin/ || RUBY_PLATFORM =~ /linux/
  config.ssh.forward_agent = true
  config.vm.provision :chef_solo do |chef|
    chef.recipe_url =
      "http://assets.querycasts.com/lab/cookbooks.tar.gz"
    chef.add_recipe("querycasts-lab")
  end
end
