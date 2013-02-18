# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.box = "querycasts-lab-0.0.1"
  config.vm.box_url =
    "http://assets.querycasts.com/lab/vms/querycasts-lab-0.0.1.box"
  config.vm.host_name = "lab"
  config.vm.network :hostonly, "33.33.33.10"
  config.vm.provision :chef_solo do |chef|
    chef.recipe_url =
      "http://assets.querycasts.com/lab/cookbooks.tar.gz"
    chef.add_recipe("querycasts-lab")
  end
end
