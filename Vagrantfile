ip = "192.168.33.198";

Vagrant.configure("2") do |config|
  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "forwarded_port", guest: 443, host: 443
  config.vm.box = "centos/7"
  config.vm.hostname = "zabbix"
  config.vm.define "zabbix"
  config.vm.network "private_network", ip: ip
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "3096"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end

