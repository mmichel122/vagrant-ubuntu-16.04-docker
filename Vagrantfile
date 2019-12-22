# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "bento/ubuntu-16.04"
  config.vm.hostname = "docker-demo"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 3306, host: 3306
 
  for i in 8081..9000
    config.vm.network :forwarded_port, guest: i, host: i
  end
 
  # Disable automatic box update checking. If you disable this, then
  # config.vm.network "private_network", ip: "10.0.2.116"
  # config.vm.box_check_update = false
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # config.vm.synced_folder "../data", "/vagrant_data"
  # config.vm.synced_folder ".", "/vagrant", type: "smb", mount_options: ["domain=" + ENV["GB"]]

  #config.vm.synced_folder ".", "/vagrant", type: "smb", mount_options: ["domain=gb.computacenter.co.uk"]

  #config.vm.synced_folder ".", "/vagrant", disabled: true 

  # Example for VirtualBox:
  #
  #config.vm.provider "virtualbox" do |vb|
     # Customize the amount of memory on the VM:
   #  vb.memory = "1024"
   #end.

  # Enable provisioning with a shell script. Additional provisioners such as
   config.vm.provision "shell", 
   path: "script.sh"
  
end
