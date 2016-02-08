$script = <<SCRIPT
sudo apt-get install -qq -y python-pip python-dev
sudo pip install ansible==1.9.4
echo -ne "[defaults]\nroles_path=/opt/ansible_roles\n" > /home/vagrant/.ansible.cfg
sudo mkdir -p /opt/ansible_roles
sudo ln -fTs /vagrant /opt/ansible_roles/ansible-role-authy-ssh
SCRIPT

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.provision "shell", inline: $script

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "tests/test.yml"
    ansible.install = false
  end
end
