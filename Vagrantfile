# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.define "elixir_box" do |elixir_box|
    elixir_box.vm.provider "vmware_fusion" do |v|
      v.vmx["memsize"] = 4096
      v.vmx["numvcpus"] = 4
    end
    
    
    elixir_box.vm.network :public_network
    elixir_box.vm.provision :shell, :path => "vagrant_provision.sh"
  end
end
