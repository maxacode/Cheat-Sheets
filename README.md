# Cheat-Sheets

[Great Source: devhints](https://devhints.io/)


# Terminal Cheat sheets
- cheat.sh/{Service/Cmnd/Program}


# Misc Commands:

### SSh
- ssh-keygen | create a new public/private key
- mkdir .ssh
- nano .ssh/authorized_keys | Add public keys that are authorized here. 
- nano /etc/ssh/sshd_config
- ssh -i ~/.ssh/id_somehubs user@host | Allows specifing custom key. 

### Sudo not found
su -
apt install sudo
usermod -aG sudo <username>
exit
/etc/ssh/sshd_config
  
### Speed test CLI
- https://www.speedtest.net/apps/cli
  ### ubuntu/debian
- sudo apt-get install curl
- curl -s https://install.speedtest.net/app/cli/install.deb.sh | sudo bash
- sudo apt-get install speedtest
  
  ### Mac
- brew tap teamookla/speedtest
- brew update
- brew uninstall speedtest --force
- brew install speedtest --force
