theme: jekyll-theme-minimal
Description: This will go over the installation of Docker through the inital use of Ubuntu and then through a different number of options in regards for the project.

# Comments and Complaints marked by #
# Again, this is for installing on an Ubuntu Server terminal

1. sudo apt update # The first command from here

2. sudo apt install ca-certificates curl gnupg lsb-release

3. curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

4. echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] 
         https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/nul

5. sudo apt update

6. sudo apt install docker-ce docker-ce-cli containerd.io

7. sudo usermod -aG docker admin  # Last step but an issue I had at first was the "admin" input, replace "admin" with your username that you use for Ubuntu

# 7 is the last command for installing on an Ubuntu Server

# From here we install Docker Compose;
# Since we will assume that we didn't choose the Windows/Mac version the steps are that follows for Linux

1. sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

2. sudo chmod +x /usr/local/bin/docker-compose

# You should now be able to test and see if compose is available using the command: docker-compose --version

Option A: OpenVAS/Greenborne Docker

Inital steps: 1) sudo apt-get update 2) sudo apt-get upgrade 3) sudo apt-get install docker.io
(From the given links in Harvey; 
https://utulsa.hosted.panopto.com/Panopto/Pages/Embed.aspx?id=75912983-0806-47a5-a3ad-acc9018aaec3 
https://github.com/mikesplain/openvas-docker)


1) Installing the contianer has the command [sudo docker run -d -p 443:443 --name openvas mikesplain/openvas] (Please wait 10-20 minutes during this time)

2) Now go to your local web browser and enter https://localhost and you will get a warning for potential security risk.
   Go to the advanced button and click to continue and you will enter the webpage for OpenVAS/Greenborne;
   Username and Password are both "Admin"
   
         
# Docker Run converted to docker-compose
Original is [sudo docker run -d -p 443:443 --name openvas mikesplain/openvas]

Which is then converted to the following:

version: '3.3'
services:
    openvas:
        ports:
            - '443:443'
        container_name: openvas
        image: mikesplain/openvas
