Vagrant.configure("2") do |config|

  config.vm.define "manager" do |manager|
    manager.vm.box = "ubuntu/focal64"
    manager.vm.hostname = "manager"
    manager.vm.network "private_network", ip: "192.168.10.10"
    manager.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.box = "ubuntu/focal64"
    worker1.vm.hostname = "worker1"
    worker1.vm.network "private_network", ip: "192.168.10.11"
    worker1.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.box = "ubuntu/focal64"
    worker2.vm.hostname = "worker2"
    worker2.vm.network "private_network", ip: "192.168.10.12"
    worker2.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

end
