# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty32"
 
  config.omnibus.chef_version = :latest

  config.vm.provision :chef_solo do |chef| 
    chef.log_level = :debug    
#    chef.cookbooks_path = "~/Dropbox/chef/cookbooks" 

    chef.add_recipe ("apt")   
    chef.add_recipe ("git")
#    chef.add_recipe "build-essential"
#    chef.add_recipe "ruby_build"
#    chef.add_recipe "rbenv::vagrant"
#    chef.add_recipe "rbenv::user"

    chef.json = {
      'rbenv' => {
        'user_installs' => [
          {
            'user'    => 'vagrant',
            'rubies'  => ['2.0.0-p247'],
            'global'  => '2.0.0-p247',
            'gems'    => {
              '2.0.0-p247' => [
                { 'name'    => 'bundler' },
                { 'name'    => 'rails' },
                { 'name'    => 'haml' }
              ]
            }
          }
        ]
        }
      }
  end
end