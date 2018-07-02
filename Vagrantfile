Vagrant.configure(2) do |config|  
  config.vm.define "nodejs" do |nodejs|
    nodejs.vm.box = "ubuntu/xenial64"
    nodejs.vm.hostname = "nodejs"
    nodejs.vm.network "private_network", ip:"192.168.50.4" 
    nodejs.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"  
    end     
        nodejs.vm.provision "shell", inline: <<-SHELL
        sudo apt-get update
	curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
	sudo apt-get install -y nodejs	
	git clone https://github.com/ZeroFuntom/M901.git
	sudo chmod -R 777 M901
	cd ~/M901/src/client/shop
	npm install
	cd src/app
	npm start
        #sudo reboot
        sudo apt-get -y install ufw gufw 
        sudo ufw allow from 10.0.2.2 to any port 22
	sudo ufw allow from 10.0.2.2 to any port 4200

        sudo ufw --force enable    
SHELL
    end  
 end
