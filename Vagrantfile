Vagrant.configure("2") do |config|

# # # configuration for comman Machine
  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"
  config.disksize.size = "10GB"
  config.vm.synced_folder "/tmp", "/tmp"
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "1024"]
    vb.customize ["modifyvm", :id, "--cpus", "1"]
  end


####### Machine :1
  config.vm.define "M1" do |config|
    config.vm.hostname = "M1"
    config.vm.box = "ubuntu/bionic64"
    config.vm.network "public_network", bridge: "wlp3s0" , ip: "192.168.0.112"

# # # Hardware for M1
    
    #config.vm.provider :virtualbox do |vb|
    #  vb.customize ["modifyvm", :id, "--memory", "2048"]
    #  vb.customize ["modifyvm", :id, "--cpus", "1"]
    #end
  end
###############################################################

####### Machine :2
  config.vm.define "M2" do |config|
    config.vm.hostname = "M2"
    config.vm.box = "ubuntu/bionic64"
    config.vm.network "public_network", bridge: "wlp3s0" , ip: "192.168.0.113"
# # # Hardware for M2
    
    #config.vm.provider :virtualbox do |vb|
    #  vb.customize ["modifyvm", :id, "--memory", "2048"]
    #  vb.customize ["modifyvm", :id, "--cpus", "1"]
    #end
  end
###############################################################
  
 # config.vm.box = "base"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  config.vm.box_check_update = true

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "/tmp", "/tmp"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:
  #
  # config.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
  #   vb.gui = true
  #
  #   # Customize the amount of memory on the VM:
  #   vb.memory = "1024"
  # end
  #
  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  #config.vm.provision "shell", inline: <<-SHELL
  #	 sudo timedatectl set-timezone Asia/Kolkata 
  #  sudo apt-get update
  #  apt-get install -y apache2
   #SHELL
end
