project_name = "pwspace"

Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise32"
  config.vm.synced_folder ".", "/vagrant"
  config.vm.provision :shell, path: ".vagrant/bootstrap.sh"
  config.vm.network :forwarded_port, host: 4019, guest: 80
  config.vm.provider "virtualbox" do |v|
    v.name = "PDub Dev"
    v.gui = false
  end
end
