# -*- mode: ruby -*-
# vi: set ft=ruby :

hosts = {
  'larry' => '192.168.88.10',
  'curly' => '192.168.88.11',
  'moe' => '192.168.88.12'

}

Vagrant.configure("2") do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  hosts.each do |name,ip|
    config.vm.define name do |machine|
      machine.vm.network :private_network, ip: ip
      machine.vm.provider 'virtualbox' do |v|
        v.name = name
      end
    end
  end
end
