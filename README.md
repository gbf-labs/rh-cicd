# Install Pylint3
```bash
sudo apt install pylint3
# Run Pylint 3
pylint3 <folder-name>
# SETUP
vim ~/.pylintrc
# to include the directory above your module, like this:
[MASTER]
init-hook='import sys; sys.path.append("/path/to/root")'
# ----------------------------------------
```

# Install NodeJS
```bash
sudo apt-get install curl software-properties-common

curl -sL https://deb.nodesource.com/setup_12.x | sudo bash -

sudo apt-get install nodejs
```

# Install Docker
```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

sudo usermod -aG docker <username> # Logout after to take effect

sudo curl -L "https://github.com/docker/compose/releases/download/1.24.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```
# Install Jenkins

```bash
sudo apt-get install software-properties-common


sudo apt update
sudo apt install default-jre

wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'

sudo apt update
sudo apt install jenkins

HTTP_PORT=8080

sudo service jenkins restart

# suorce: https://stackoverflow.com/questions/21588993/how-much-ram-for-a-jenkins-master-instance)
# RUN:
sudo apt-get install git
sudo apt-get install curl

# Add the user to the docker group:
sudo usermod -a -G docker penn
sudo usermod -a -G docker jenkins
# NOTE: Completely log out of your account ang log back in again

# CHANGE PASSWORD JENKINS
sudo passwd jenkins
admin

# CHANGE PERMISSION CURRENT DIRECTORY
chmod -R 777 <dir>
```

## For RH project
```bash
ADD:
config_files/config/config.cfg
config_files/config2/config.cfg

# CREATE qa_folder FOLDER

```


## Add user to use sudo without password
```bash
visudo
ex: penn ALL=(ALL) NOPASSWD:ALL
    jenkins ALL=(ALL) NOPASSWD:ALL
```

## User jenkins access
```text
## ADD THE PERMISSION TO CLONE
## SWITCH TO JENKINS USER
ssh-keygen -t rsa
## ADD THE KEY TO GITLAB
## ADD THE KEY TO BITBUCKET
```


## After the installation of Jenkins and Docker
```bash
sudo gpasswd -a jenkins docker

# Reboot the server
sudo reboot
```