Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"   # Box do Ubuntu 20.04

  config.vm.define "vagrant-shell-script" do |machine|
    machine.vm.hostname = "vagrant-shell-script"   # Nome da máquina virtual

    machine.vm.provision "shell", inline: <<-SHELL
      # Instalação de pacotes
      apt-get update
      apt-get install -y vim curl telnet unzip wget net-tools htop nmap

      # Criação de usuário
      useradd -m leandro-goncalves
    SHELL
  end
end
