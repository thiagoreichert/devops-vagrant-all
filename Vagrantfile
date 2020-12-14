# Por Thiago Reichert

Vagrant.configure("2") do |config|

    # Configurações Globais

    config.vm.provider "virtualbox" do |v|
        v.memory = 512
    end

    # Configurações da máquina virtual para Sistema Operacional CentOS
    config.vm.define "vm-centos" do |centos|
        centos.vm.box = "centos/7"
        centos.vm.network "private_network", ip: "192.192.10.11"
        centos.vm.synced_folder ".", "/vagrant"
        centos.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-centos
        SHELL
    end

    # Configurações da máquina virtual para Sistema Operacional Ubuntu
    config.vm.define "vm-ubuntu" do |ubuntu|
        ubuntu.vm.box = "ubuntu/trusty64"
        ubuntu.vm.network "private_network", ip: "192.192.10.12"
        ubuntu.vm.synced_folder ".", "/vagrant"
        ubuntu.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-ubuntu
        SHELL
    end

    # Configurações da máquina virtual para Sistema Operacional Debian
    config.vm.define "vm-debian" do |debian|
        debian.vm.box = "debian/jessie64"
        debian.vm.network "private_network", ip: "192.192.10.13"
        debian.vm.synced_folder ".", "/vagrant"
        debian.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-debian
        SHELL
    end

    # Configurações da máquina virtual para Docker em Sistema Operacional CentOS
    config.vm.define "vm-docker" do |docker|
        docker.vm.box = "centos/7"
        docker.vm.network "private_network", ip: "192.192.10.14"
        docker.vm.synced_folder ".", "/vagrant"
        docker.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-docker
            sudo yum install -y yum-utils
            sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo 
            sudo yum install docker-ce docker-ce-cli containerd.io -y
            sudo systemctl start docker
        SHELL
    end

    # Configuração de máquina virtual para Ansible em Sistema Operacional CentOS  
    config.vm.define "vm-ansible" do |ansible|
        ansible.vm.box = "centos/7"
        ansible.vm.network "private_network", ip: "192.192.10.15"
        #ansible.vm.synced_folder ".", "/vagrant"
        ansible.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-ansible
            rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
            yum install ansible python vim -y 
        SHELL
    end

    # Configurações da máquina virtual para Sistemas da FESC
    config.vm.define "vm-sistema1" do |sistema1|
        sistema1.vm.box = "centos/7"
        sistema1.vm.network "private_network", ip: "192.192.10.16"
        sistema1.vm.synced_folder ".", "/vagrant"
        sistema1.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-sistema1
        SHELL
    end

    # Configurações da máquina virtual para Sistemas da FESC
    config.vm.define "vm-sistema2" do |sistema2|
        sistema2.vm.box = "centos/7"
        sistema2.vm.network "private_network", ip: "192.192.10.17"
        sistema2.vm.synced_folder ".", "/vagrant"
        sistema2.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-sistema2
        SHELL
    end

    # Configurações da máquina virtual para Docker Swarm CentOS
    config.vm.define "vm-docker1" do |dockers1|
        dockers1.vm.box = "centos/7"
        dockers1.vm.network "private_network", ip: "192.192.10.20"
        dockers1.vm.synced_folder ".", "/vagrant"
        dockers1.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-docker-1
            sudo yum install -y yum-utils
            sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo 
            sudo yum install docker-ce docker-ce-cli containerd.io -y
            sudo systemctl start docker
        SHELL
    end


        # Configurações da máquina virtual para Docker Swarm em Sistema Operacional CentOS
    config.vm.define "vm-docker2" do |dockers2|
        dockers2.vm.box = "centos/7"
        dockers2.vm.network "private_network", ip: "192.192.10.21"
        dockers2.vm.synced_folder ".", "/vagrant"
        dockers2.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-docker-2
            sudo yum install -y yum-utils
            sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo 
            sudo yum install docker-ce docker-ce-cli containerd.io -y
            sudo systemctl start docker
        SHELL
    end


        # Configurações da máquina virtual para Docker Swarm em Sistema Operacional CentOS
    config.vm.define "vm-docker3" do |dockers3|
        dockers3.vm.box = "centos/7"
        dockers3.vm.network "private_network", ip: "192.192.10.22"
        dockers3.vm.synced_folder ".", "/vagrant"
        dockers3.vm.provision "shell", inline: <<-SHELL
            hostnamectl set-hostname vm-docker-3
            sudo yum install -y yum-utils
            sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo 
            sudo yum install docker-ce docker-ce-cli containerd.io -y
            sudo systemctl start docker
        SHELL
    end
end