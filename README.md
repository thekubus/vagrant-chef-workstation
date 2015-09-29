# vagrant-chef-workstation
Chef Workstation made with Vagrant and Ubuntu Trusty Tahr 32 bit. The project has all the required submodule linked under directory cookbooks.

# How to use

1. Download and install [Virtualbox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](https://www.vagrantup.com/downloads.html)
2. Create Vagrant working directory, initialize Vagrant machine, and clone this repository. In linux, run the following command from terminal session  

   ```shell
   $ md my-kitchen 
   $ cd my-kitchen  
   $ vagrant init  
   $ git clone https://github.com/thekubus/vagrant-chef-workstation.git   
   ```

3. Start Vagrant machine, and grab a cup of coffee. The startup and provisioning process will take a while, especially if you need to download the base box

# Frequently asked question

**Q: I want to use another flavor of Ubuntu**  
A: Feel free to fork this repo, and change the box that you want to use in file Vagrantfile

**Q: I want to use another linux**  
A: Same. Fork this repo and change the box that you want to use in file Vagrantfile. Note that I haven't tested this setup with other Linux flavor.
