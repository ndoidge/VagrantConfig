Vagrant.configure("2") do |config|
  config.vm.define "nxos1" do |nxos1|
    nxos1.vm.box = "nxosv"
    nxos1.vm.hostname = 'nxos1'

#    nxos1.vm.network "private_network", ip: "192.168.56.101"
    nxos1.vm.network "forwarded_port", guest: 22, host: 10122, id: "ssh"
    nxos1.vm.network "forwarded_port", guest: 80, host: 10180
    nxos1.vm.network "forwarded_port", guest: 443, host: 10143


    nxos1.vm.provider :virtualbox do |v|
      v.memory = "4096" 
    end
  end

  config.vm.define "nxos2" do |nxos2|
    nxos2.vm.box = "nxosv"
    nxos2.vm.hostname = 'nxos2'

    nxos2.vm.network "private_network", ip: "192.168.56.102"
    nxos2.vm.network "forwarded_port", guest: 22, host: 10222, id: "ssh"
    nxos2.vm.network "forwarded_port", guest: 80, host: 10280
    nxos2.vm.network "forwarded_port", guest: 443, host: 10243


    nxos2.vm.provider :virtualbox do |v|
      v.memory = "4096" 
    end
  end

end

