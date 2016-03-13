# Vagrant run
Vagrant.configure("2") do |config|

    # Box setup
    config.vm.box = "ubuntu/trusty64"
    config.vm.box_url = "https://vagrantcloud.com/ubuntu/boxes/trusty64/versions/14.04/providers/virtualbox.box"

    # Manually install ansible 1.9.2 because 2.0 is incompatibile
    # @see https://github.com/geerlingguy/drupal-vm/issues/372
    config.vm.provision "shell", inline: "sudo apt-get update && sudo apt-get install -y python-pip python-dev && sudo pip install ansible==1.9.4 && sudo cp /usr/local/bin/ansible /usr/bin/ansible"

    # Provision
    config.vm.provision "ansible_local" do |ansible|
        ansible.install = false # we already installed it earlier
        ansible.playbook = "ansible/play.yml"
    end

end
