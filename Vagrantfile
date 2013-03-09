# -*- mode: ruby -*-
# http://vagrantup.com/

require 'berkshelf/vagrant'

VM_RAM_MB = ENV.fetch 'SHARPSAW_VM_MB', 2

Vagrant::Config.run do |config|
  config.vm.box = 'precise64'
  config.vm.boot_mode = :gui unless ENV['nogui']
  # TODO: Figure out an internal host for the base.box
  config.vm.box_url = 'http://cloud-images.ubuntu.com/vagrant/precise/current/precise-server-cloudimg-amd64-vagrant-disk1.box'

  # config.vm.share_folder 'hosttmp', '/hosttmp', '/tmp'
  config.vm.customize ['modifyvm', :id, '--memory', VM_RAM_MB * 1024]

  #config.vm.forward_port 3000, 3300

  # config.vm.provision :chef_solo do |chef|
  # end
end
# vim:ft=ruby
