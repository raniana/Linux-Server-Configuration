# Linux-Server-Configuration project

<p>IP address of Lightsail instance: 52.15.210.121
<p>SSH port: 2200
<p>Web App URL: http://ec2-52-15-210-121.us-east-2.compute.amazonaws.com/

## Summary of Software and Configuration Changes:

* All currently installed packages were updated.
* In the file sshd_config the ssh port was changed to 2200.
* The ufw was configured to allow SSH through port 2200 and HTTP on port 80.
* The same settings were applied to the instance's Firewall on the lightsail website.
* The private key of the ubuntu user was downloaded from the website and used to ssh through the terminal.
* A new user 'grader' was created and given sudo priviledge.
* A key pair was created ssh-keygen tool, to grant access for this user.
* Apache HTTP server was installed.
* Python 3 mod-wsgi installed.
* libapache2-mod-wsgi installed.
* mod-wsgi was enabled.
* Postgresql installed.
* A new database user 'Catalog' was created with a password.
* An empty database was created and owned by user 'Catalog'.
* git was installed.
* Item-Catalog web app was cloned to the lightsail virtual machine and located on: /var/www/Catalog/Catalog.
* Using pip virtualenv was installed to host the flask framework.
* Virtualenv was activated and Flask was installed.
* /etc/apache2/sites-available/Catalog.conf file was created and configured to enable a new virtual host with the Lightsail instance IP address.
* The virtual host was enabled from the terminal. 
* The .wsgi file was created to serve the flask app and placed in the Catalog repo.
* The Apache server was restarted.
* The Catalog data base was populated with data using populatedatabase.py file.
* Access to .git directory through the website was disabled by placing .htaccess file in the .git directory.

## Resources:

* Udacity Forum
* https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps
* https://stackoverflow.com/questions/6142437/make-git-directory-web-inaccessible

## Local key is loacted on file :

/home/grader/.ssh/authorized_keys
