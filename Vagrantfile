
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.50.55"
  config.vm.synced_folder ".", "/Samuel-Examen-Tema7"

  config.vm.provision "shell", inline: <<-SHELL

    sudo apt-get install -y php php-mysqli

    echo "-- Insertar datos de ejemplo en la lista 'menu'" > /home/vagrant/datos_menu.sql
    echo "INSERT INTO gestion_restaurante.menu (primer_plato, segundo_plato, postre, precio) VALUES" >> /home/vagrant/datos_menu.sql
    echo "('Rodaballo', 'Lubina', 'Tarta de la abuela', 45)," >> /home/vagrant/datos_menu.sql
    echo "('Cachopo', 'Merluza', 'Tarta de queso', 50)," >> /home/vagrant/datos_menu.sql
    echo "('Fabada', 'Chuleton', 'Arroz con leche', 30)," >> /home/vagrant/datos_menu.sql

  SHELL

end
