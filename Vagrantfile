Vagrant.configure("2") do |config|

    #Base box
    config.vm.box = "generic/debian12"
  
    # Networking - Private network using dynamic IP
    config.vm.network "private_network", ip:"192.168.10.10"
  
    # Windows-specific workaround for ansible_local provisioner to use the project's ansible.cfg
    config.vm.synced_folder ".", "/vagrant",  mount_options: ["dmode=775,fmode=755"]
    
    #Configuring VM
    config.vm.provider "virtualbox" do |vb|
  
      vb.gui = true
      vb.memory = "1024"
  
    end
  
    #ansible
    #config.vm.provision "ansible_local" do |ansible|
    #  ansible.install = true
    #  ansible.playbook = "playbook.yml"
    #end
  end