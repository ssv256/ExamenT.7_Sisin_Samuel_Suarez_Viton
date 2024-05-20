
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  config.vm.synced_folder ".", "/Samuel-Examen-Tema7"

  config.vm.provision "shell", inline: <<-SHELL

    sudo apt-get install -y php php-mysqli


  SHELL

end
