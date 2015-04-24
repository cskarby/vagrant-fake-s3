# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

$script = <<END
gem install fakes3
echo "#!/bin/sh -e" > /etc/rc.local
echo "/usr/local/bin/fakes3 -r /vagrant/fake_s3_root -p 8080 2>&1 |logger -t fakes3 &" >> /etc/rc.local
service rc.local start
END

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "trusty64"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.provision "shell", inline: $script
end
