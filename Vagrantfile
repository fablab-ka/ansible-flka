VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "felix", primary: true do |host|
    host.vm.box = "ubuntu/trusty64"

    host.vm.provision :ansible do |ansible|
      ansible.sudo = true
      ansible.playbook = "felix.yml"
    end
  end

  config.vm.define "lasersaur" do |host|
    host.vm.box = "ubuntu/trusty64"

    host.vm.provision :ansible do |ansible|
      ansible.sudo = true
      ansible.ask_vault_pass = true
      ansible.playbook = "lasersaur.yml"
    end
  end

end
