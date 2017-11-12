# PHP 7, Apache, MySQL (LAMP) docker environment  - for Parrot Tunes (Open Web Media Library and Player)


Docker container with php 7 on Apache (httpd) MySQL. https://bitbucket.org/rocean/owmp
Based on an docker-compose.yml file


# Requirements
- Docker
- Virtualbox (mostly comes / gets installed with docker)
- GIT
- Little bit of git knowledge (to clone)

This configution is made on `OSX` but should be working in every other operating system

Note this document is based on the standard first up of docker (192.168.99.100) if this is different for your current situation please replace all IP addresses in your setup too.

Go to your terminal and Clone or fork the project.

cd /www
git clone https://github.com/dsphinx/docker-owmp.git
cd docker-owmp/
docker-compose up -d


Now open your browser and go to: `http://host1.local/`
in your browser you should see a PHP 7 info page. 



You can add more `Virtual Hosts` in `etc/apache2/hosts.conf` the host1.local is in there.

When you want to change the database name and password take a look into `docker-compose.yml`

# Multiple databases
So far docker has no support for creating the databases with the .yml file. In this repo I created a folder called mysql which you can find in `etc/mysql` when you place your sql files in here, these will automatically be loaded when you start your docker
