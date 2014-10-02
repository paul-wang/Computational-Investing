# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

$script = <<SCRIPT
wget http://pypi.python.org/packages/source/Q/QSTK/QSTK-0.2.8.tar.gz
tar -xzvf QSTK-0.2.8.tar.gz
cd QSTK-0.2.8
sudo sh UbuntuInstallation.sh
sudo python setup.py install
SCRIPT


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "box-cutter/ubuntu1204-desktop"
  config.vm.provider "virtualbox" do |vb|
     vb.gui = true
  end
  config.vm.provision :shell, :inline => $script, privileged: false
end
