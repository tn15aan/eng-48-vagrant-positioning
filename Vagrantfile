Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.100"
  config.hostsupdater.aliases = ["development.local"]

  #sync a folder
  #to_sync_folder, #to_sync_vm
  config.vm.synced_folder "app", "/app"

  # provisioning
  config.vm.provision "shell", path: "environment/provision.sh"
end
