# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.provision :shell, :path => "provision.sh"
  config.ssh.forward_agent = true
  config.vm.network "forwarded_port", guest: 8000, host: 1236
  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
  end
end