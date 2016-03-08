
Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.define "erwp" do |erwp|
    erwp.vm.provision :ansible do |ansible|
      ansible.playbook = "site.yml"
    end

    erwp.vm.network :forwarded_port, guest: 80, host: 8888, auto_correct: true
  end
end
