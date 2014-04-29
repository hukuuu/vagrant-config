Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise32"
  config.vm.synced_folder "srv/", "/srv/"
  config.vm.provision :salt do |salt|
    salt.minion_config = "srv/minion"
    salt.run_highstate = true
  end
end

Vagrant::Config.run do |config|
  config.vm.forward_port 3000, 3000
end