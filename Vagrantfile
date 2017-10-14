Vagrant.configure("2") do |config|
  config.vm.box = "31z4/boot2docker"

  config.vm.provision "shell", path: "scripts/wait-for-docker.sh"

  config.vm.define "manager1", primary: true do |manager1|
    manager1.vm.network "private_network", ip: "192.168.50.100"
    manager1.vm.hostname = "manager1"

    manager1.vm.provision "shell", path: "scripts/manager.sh" do |s|
      s.args = ["192.168.50.100"]
    end
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.network "private_network", ip: "192.168.50.101"
    worker1.vm.hostname = "worker1"

    worker1.vm.provision "shell", path: "scripts/worker.sh" do |s|
      s.args = ["192.168.50.101", "192.168.50.100:2377"]
    end
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.network "private_network", ip: "192.168.50.102"
    worker2.vm.hostname = "worker2"

    worker2.vm.provision "shell", path: "scripts/worker.sh" do |s|
      s.args = ["192.168.50.102", "192.168.50.100:2377"]
    end
  end
end
