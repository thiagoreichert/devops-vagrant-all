# Vagrant

## Sobre Vagrant
O HashiCorp Vagrant é um software de código aberto para criar e manter ambientes de desenvolvimento virtuais portáteis, utilizando VirtualBox, KVM, Hyper-V, Docker containers, VMware, e AWS. Simplifica através de arquivos de configurações a gerência de de software das virtualizações para aumentar a produtividade do desenvolvimento.

Documentação https://docs.vagrantup.com

## Requisitos
Download Vangrant: https://www.vagrantup.com/

Download VirtualBox: https://www.virtualbox.org/ (Pode ser utilizados outros virtualizadores como KVM, Hyper-V, VMWare. AWS)

OBS: Para realizar a instalação do VirtualBox pode ser necessário desabilitar o antivírus da máquina.

Para quem estiver utilizando windows é necessário possuir algum interpretador de comandos Bash, como terminal do Git Bash ou Virtual Studio Code.

## Imagens Públicas
É possível utilizar boxes fornecidos pelo próprio Vagrant, não sendo necessário criar imagens próprias para utilização do sistema.

https://app.vagrantup.com/boxes/search

## VMs disponíveis nesta configuração
vm-centos	192.192.10.11	CentOS 7.8 - 64	Testes com VM CentOS limpo. 

vm-ubuntu	192.192.10.12	Ubuntu Trusty 14.04 - 64	Testes com VM Ubuntu limpo. 

vm-debian	192.192.10.13	Debian 8 - 64	Testes com VM Debian limpo. 

vm-docker	192.192.10.14	CentOS 7.8 - 64	VM com docker já instalado e configurado.

vm-ansible	192.192.10.15	CentOS 7.8 - 64	VM com ansible já instalado e configurado.

vm-sistema1	192.192.10.16	CentOS 7.8 - 64	VM para testes realizados pelo ansible.

vm-sistema2	192.192.10.17	CentOS 7.8 - 64	VM para testes realizados pelo ansible.

vm-docker1   192.192.10.20   CentOS 7.8 - 64	VM para utilização de docker swarm.

vm-docker2   192.192.10.21   CentOS 7.8 - 64	VM para utilização de docker swarm.

vm-docker3   192.192.10.22   CentOS 7.8 - 64	VM para utilização de docker swarm.

## Configuração na máquina host
Criar diretório chamado vagrant e baixar o Vagrantfile no projeto do Git.

No diretório executar o comando 'vagrant status' para verificar se o arquivo está correto e então 'vagrant up' para subir a VM que deseja.

## Compartilhamento de arquivos
Para compartilhar arquivos da máquina host para a máquina virtual basta adicionar os arquivos no diretório vagrant. Na máquina host o arquivo estará em /vagrant.

## Principais comandos
Os comandos sempre devem ser executados no diretório que se encontra Vagrantfile. No windows deve ser utilizado Virtual Studio Code ou Git Bash.

vagrant status - Apresenta lista com nomes e estado de cada VM.

vagrant up $NOME_DA_VM - Sobe uma VM não criada, suspensa ou desligada.

vagrant halt $NOME_DA_VM - Desliga uma VM específica. Se não passar o nome da VM desliga todas as VMs.

vagrant destroy $NOME_DA_VM - Destrói a VM, ou seja, remove a VM do Virtual Box.

vagrant ssh $NOME_DA_VM - Acessa via ssh uma VM que esteja ligada.

vagrant snashot $NOME_DA_VM - Cria snapshot da VM.

