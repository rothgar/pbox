# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure(2) do |config|
  config.vm.box = "rothgar/firefox"

  config.vm.synced_folder "upload", "/home/vagrant/Documents",
    owner: "vagrant", group: "vagrant", create: "true",
    mount_options: ["ro"]

  config.vm.synced_folder "download", "/home/vagrant/Downloads",
    owner: "vagrant", group: "vagrant", create: "true"

  # Configure virtualbox provider
  config.vm.provider "virtualbox" do |vb|
    #   # Display the VirtualBox GUI when booting the machine
    vb.gui = true
    vb.name = "pbox-firefox"
    vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
    vb.customize ["modifyvm", :id, "--audio", "pulse"]
    vb.customize ["modifyvm", :id, "--audiocontroller", "hda"]
    # 17MB vram required for seemless mode
    vb.customize ["modifyvm", :id, "--vram", "24"]
    #   # Customize the amount of memory on the VM:
    #   vb.memory = "1024"
  end

end
