# Autoinstall T-Pot on Ubuntu 16.04.x 
This script will install [T-Pot 17.10](http://dtag-dev-sec.github.io/mediator/feature/2017/11/07/t-pot-17.10.html) on a fresh Ubuntu 16.04.x LTS (64bit). 

It is intended to be used on hosted servers, where an Ubuntu base image is given and there is no ability to install custom ISO images. 
Successfully tested on vanilla Ubuntu 16.04.3 in VMware.

Choose Ubuntu 16.04.x 64bit as operating system. Make sure you have your SSH key added to your account (~/.ssh/authorized_keys) 
and meet the [system requirements](http://dtag-dev-sec.github.io/mediator/feature/2017/11/07/t-pot-17.10.html#requirements) (>=4GB RAM, 64GB disk, network exposure) for a full T-Pot instance. The system requirements depend on the flavour of T-Pot you intend to run. 

During setup, you can choose from four different configurations: T-Pot's standard installation, industrial edition, full installation and, in case you have limited ressources, you can opt for a "honeypot only"-mode during install, which will install T-Pot without suricata and ELK dashboard (>=3GB RAM required). 

So, clone the repository. Run as root. Enjoy.

    git clone https://github.com/Sy14r/t-pot-autoinstall.git
    cd t-pot-autoinstall/
    sudo su
    ./install.sh
    
If you run into problems during installation it might be related to your hoster's custom Ubuntu update repositories. So far, we do not have a solution for this. 

Due to public demand, we added a non-interactive installation option. Just add the *username*, the *number referencing the edition* and the *password for web access* to the installation script, e.g.

	./install.sh ubuntu 2 myPassw0rd
		
will install the **Honeypot Only Edition** (2) for the user "ubuntu" and set the web access password to "myPassw0rd". 


	

	
