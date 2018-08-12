
Vagrant.configure("2") do |config|
  config.vm.define "web" do |web|

  	web.vm.box = "centos/7"
  	web.vm.provision :shell, path: "bootstrap.sh"
  	web.vm.network :forwarded_port, guest: 80, host: 8080
 	web.vm.network :forwarded_port, guest: 8081, host: 8081

  	web.vm.network "private_network", ip: "192.168.33.10"
  	web.vm.synced_folder ".", "/vagrant"
  end
end
