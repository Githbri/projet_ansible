  Vagrant.configure("2") do |config|
  config.vm.box = "centos/stream9"
  config.vm.network "private_network", ip: "10.0.0.15"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
  end
  config.vm.network "forwarded_port", guest: 3000, host: 3000
end
