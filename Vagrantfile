Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"
  config.vm.hostname = "zabbix"
  config.vm.define "zabbix"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "3096"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end

