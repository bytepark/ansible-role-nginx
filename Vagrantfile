Vagrant.configure(2) do |config|
  config.vm.define 'ansible-role-nginx' do |machine|
    machine.vm.box = "ubuntu/precise32"
    #machine.vm.box = "ubuntu/trusty64"

    machine.vm.provision "ansible" do |ansible|
      ansible.playbook = "tests/test.yml"
      ansible.sudo = true
      ansible.verbose = ENV['ANSIBLE_VERBOSE'] ||= "v"
      ansible.tags = ENV['ANSIBLE_TAGS'] ||= "all"
    end
  end
end