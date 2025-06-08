Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: <<-SHELL
    echo "10.0.5.10 devops" >> /etc/hosts
 SHELL

  config.vm.define "devops" do |devops|
    devops.vm.box = "ubuntu/jammy64"
    devops.vm.hostname = "devops"
    devops.vm.network "private_network", ip: "10.0.5.10"
    devops.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
  end
end
