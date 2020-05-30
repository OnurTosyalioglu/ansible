#-*- mode: ruby -*-

BOX="ubuntu/bionic64"
CPU=1
MEMORY=512

Vagrant.configure("2") do |config|

  config.vm.define "web_lb" do |web_lb|
    web_lb.vm.box = BOX
    web_lb.vm.host_name = "weblb"
    web_lb.vm.network "private_network", ip:"11.11.11.10"

    web_lb.vm.provider :virtualbox do |vb|
        vb.memory = MEMORY
        vb.cpus = CPU
        vb.name = "WEBLB"
        vb.gui = false
    end
  end

  config.vm.define "web_1" do |web_1|
    web_1.vm.box = BOX
    web_1.vm.host_name = "web1"
    web_1.vm.network "private_network", ip:"11.11.11.11"

    web_1.vm.provider :virtualbox do |vb|
        vb.memory = MEMORY
        vb.cpus = CPU
        vb.name = "WEB1"
        vb.gui = false
    end
  end

  config.vm.define "web_2" do |web_2|
    web_2.vm.box = BOX
    web_2.vm.host_name = "web2"
    web_2.vm.network "private_network", ip:"11.11.11.12"

    web_2.vm.provider :virtualbox do |vb|
        vb.memory = MEMORY
        vb.cpus = CPU
        vb.name = "WEB2"
        vb.gui = false
    end
  end

  config.vm.define "db_lb" do |db_lb|
    db_lb.vm.box = BOX
    db_lb.vm.host_name = "dblb"
    db_lb.vm.network "private_network", ip:"10.10.10.10"

    db_lb.vm.provider :virtualbox do |vb|
        vb.memory = MEMORY
        vb.cpus = CPU
        vb.name = "DBLB"
        vb.gui = false
    end
  end

  config.vm.define "db_1" do |db_1|
    db_1.vm.box = BOX
    db_1.vm.host_name = "db1"
    db_1.vm.network "private_network", ip:"10.10.10.11"

    db_1.vm.provider :virtualbox do |vb|
        vb.memory = MEMORY
        vb.cpus = CPU
        vb.name = "DB1"
        vb.gui = false
    end
  end

  config.vm.define "db_2" do |db_2|
    db_2.vm.box = BOX
    db_2.vm.host_name = "db2"
    db_2.vm.network "private_network", ip:"10.10.10.12"

    db_2.vm.provider :virtualbox do |vb|
        vb.memory = MEMORY
        vb.cpus = CPU
        vb.name = "DB2"
        vb.gui = false
    end
  end
  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

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
  # config.vm.synced_folder "../data", "/vagrant_data"

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
  # Ansible, Chef, Docker, Puppet and Salt are also available. Please see the
  # documentation for more information about their specific syntax and use.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
