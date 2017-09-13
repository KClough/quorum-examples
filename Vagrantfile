Vagrant.configure(2) do |config|
  # config.vm.box = "ubuntu/xenial64"
  config.vm.box = "digital_ocean"
  config.vm.provider :digital_ocean do |provider, override|
    provider.ssh_key_name = "KClough MBP"
    override.ssh.private_key_path = '~/.ssh/id_rsa'
    override.vm.box = 'digital_ocean'
    override.vm.box_url = "https://github.com/devopsgroup-io/vagrant-digitalocean/raw/master/box/digital_ocean.box"
    provider.token = ''
    provider.image = 'ubuntu-16-04-x64'
    provider.region = 'nyc3'
    provider.size = '4gb'
  end
  config.vm.provision :shell, path: "vagrant/bootstrap.sh"
  config.vm.network "forwarded_port", guest: 22000, host: 22000
  config.vm.network "forwarded_port", guest: 22001, host: 22001
  config.vm.network "forwarded_port", guest: 22002, host: 22002
  config.vm.network "forwarded_port", guest: 22003, host: 22003
  config.vm.network "forwarded_port", guest: 22004, host: 22004
  config.vm.network "forwarded_port", guest: 22005, host: 22005
  config.vm.network "forwarded_port", guest: 22006, host: 22006
  config.vm.provider "virtualbox" do |v|
    v.memory = 4096
  end
end
