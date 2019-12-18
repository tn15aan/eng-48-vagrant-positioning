## README
# Steps to use this program
1. Download Vagrant and Oracle VM Virtualbox

2. Using BASH Commands navigate to the folder where you want to install your virtual machine

3. Use the command 'vagrant init' which is a command used to initialize the current directory to be a Vagrant environment by creating an initial Vagrantfile

4. Once you have the file in your folder, use the command 'vagrant up' which creates and configures guest machines according to your Vagrantfile

5. Open up your vagrant file created and configure your environment: (you can open the vagrant file using atom by using the command 'atom .')
- 'config.vm.box =' this will configure what box the machine will be brought up against eg. config.vm.box = "ubuntu/xenial64". Boxes are the package format for Vagrant environments. A box can be used by anyone on any platform that Vagrant supports to bring up an identical working environment.

- 'config.vm.network' this configures the network on the machine eg. config.vm.network "private_network", ip: "192.168.10.100"

- To alias your ip address, you will need ' config.hostsupdater.aliases' which will look like
  config.hostsupdater.aliases = ["development.local"]. The square brackets allows you to list multiple hosts, if you only want one you can use config.vm.hostname.

6. You then need to save this and then reload vagrant 'reload vagrant' and then 'vagrant up' or alternatively you could 'vagrant destroy' to stop the running machine Vagrant is managing and destroys all the resources that were created during the machine creation progress

7. You can add provision your project which allows you to define the state of the IT infrastructure. To do this you need to create a new .sh file

8. 7. Use 'vagrant ssh' in the Vagrantfile directory to gain access to the shell. From here you can navigate to files in the virtual machine and run package.json files by using npm install which installs all the local dependencies and npm start which will run node server.js
