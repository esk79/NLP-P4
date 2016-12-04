# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.synced_folder "./qa-system", "/home/vagrant/qa-system"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "6144"
    vb.cpus = "2"
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y git curl wget htop build-essential gdb valgrind
    sudo apt-get install -y python-setuptools python-dev build-essential
    sudo apt-get install -y python python-dev libatlas-base-dev gcc gfortran g++
    sudo apt-get install -y python-pip
    sudo apt-get install -y python-scipy
    sudo pip install numpy
    sudo pip install scipy
    sudo easy_install -U gensim
    sudo pip install boto
    sudo pip install nltk==3.2.1
    sudo pip install Unirest==1.1.7
    #wget https://docs.google.com/uc?export=download&confirm=tVVS&id=0B7XkCwpI5KDYNlNUTTlSS21pQmM
  SHELL
end

