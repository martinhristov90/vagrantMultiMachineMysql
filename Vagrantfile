nodes = [

    { :hostname => 'web1', :ip => '192.168.1.1', :box => 'martinhristov90/ubuntu1604' },
    { :hostname => 'web2', :ip => '192.168.1.2', :box => 'martinhristov90/ubuntu1604' },
    { :hostname => 'mysql', :ip => '192.168.1.3', :box => 'martinhristov90/ubuntu_mysql' },

    
]

Vagrant.configure("2") do |config|
nodes.each do |node|
        config.vm.define vm_name = node[:hostname] do |nodeconfig|
            nodeconfig.vm.box = node[:box]
            nodeconfig.vm.hostname = node[:hostname]
            nodeconfig.vm.network :private_network, ip: node[:ip]
            memory = node[:ram] ? node[:ram] : 256;

            nodeconfig.vm.provider "virtualbox" do |vb|
                vb.customize [
                    "modifyvm", :id,
                    "--cpuexecutioncap", "50",
                    "--memory", memory.to_s,
                  ]
            end
        end
end
end