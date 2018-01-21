# @author Khayam Gondal kanjam@g.clemson.edu

$startovs = <<SCRIPT
    sudo /etc/init.d/openvswitch-switch start
SCRIPT

Vagrant.configure("2") do |config|
    config.vm.box = "khayamgondal/genidemo"
    config.vm.box_version = "0.1"

  config.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpuexecutioncap", "100"]
      v.customize ["modifyvm", :id, "--memory", "4096"]
      v.cpus = 4

  end

  ## Guest config
  config.vm.hostname = "e2e"
  config.vm.network :private_network, type: "dhcp"


  ## Provisioning

  ## SSH config
  config.ssh.forward_x11 = true
  config.ssh.forward_agent = true

end
