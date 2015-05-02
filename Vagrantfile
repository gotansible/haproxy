# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
	config.vm.define "haproxy" do |haproxy|
		haproxy.vm.hostname = "haproxy"
		haproxy.vm.box = "hashicorp/precise64"
		haproxy.vm.provision :ansible do |ansible|
			ansible.playbook = "test.yml"
		end
		haproxy.vm.network "private_network", ip: "192.168.50.20"
	end
end
