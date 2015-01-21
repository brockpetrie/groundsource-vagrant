# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.include_offline = false

  config.vm.network :private_network, ip: '192.168.177.178'
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.hostname = 'groundsource'
  config.hostmanager.aliases = %w(groundsource.dev www.groundsource.dev)

  config.vm.synced_folder './app', '/home/vagrant/app', nfs: true

end
