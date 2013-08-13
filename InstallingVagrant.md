## How to setup Vagrant to work with WET-BOEW v4.0
This is just a basic intro to setting up Vagrant with Nodejs and git using the shell. 
First download Vagrant for your os and install it from their [website](vagrantup.com)

After it's installed open up a shell (powershell, terminal, etc...)
1. Navigate to the directory you want to run vagrant in and run type 
    vagrant init

2. Install the vagrant box of your choice I've installed Ubuntu 12.04 Precise Pangolin

    vagrant box add base http://files.vagrantup.com/precise64.box

3. Bring up the vagrant box

    vagrant up

4. When it's up login to the machine

    vagrant ssh 

5. run the following commands to get your environment setup

    sudo apt-get update
    
    sudo apt-get install git python-software-properties python g++ make -y
    
    sudo add-apt-repository ppa:chris-lea/node.js
    
    sudo apt-get update
    
    sudo apt-get install nodejs -y

6. Then clone the git repo of WET-BOEW 

    git clone https://github.com/wet-boew/wet-boew.git -b v4.0

7. Install Node packages

    cd wet-boew
    
    npm install
    
    npm install grunt-cli -g
    
    npm install grunt --save-dev

8. Run grunt init to build the package

    grunt init
    
My next step is to automate these using a provisioning tool like chef or puppet.






