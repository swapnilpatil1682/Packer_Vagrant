# Packer_Vagrant

This is complete working code for packer to vagrant

First Install packer then set path in  ~/.bashrc

export PATH=$PATH:/home/administrator/packer_install

Then run following

packer build -only=virtualbox-iso ubuntu.json

==================================================
To Create/add box to Vagrant

vagrant box add USER/BOX

vagrant box add packer-test packer_virtualbox-iso_virtualbox.box
vagrant box add va13 /home/administrator/packer_p4/ 

vagrant init packer-test
vagrant up
===================================================
To run again 

vagrant up
vagrant provision
vagrant reload --provision
vagrant ssh
====================================================
To SSH to your vagrant box

add port that generated while creating vagrant box
ssh vagrant@127.0.0.1 -p 2222
Login with username and password vagrant vagrant
====================================================
To see GUI Add below property in Vagrantfile 

config.vm.provider "virtualbox" do |v|
  v.gui = true
end
====================================================
To get list of all current boxes

vagrant box list
====================================================
To know Id of vagrant process

vagrant global-status
vagrant status f951cd7
===================================================
To package a box for Virtual box 

First shutdown the vagrant machine by following command

vagrant halt

Then ---
vagrant package --output /home/administrator/packer_p4/build/ubuntu.box (This is path where you want to store box)
=====================================================
Command to get all installed softwares from Centos

yum list installed



