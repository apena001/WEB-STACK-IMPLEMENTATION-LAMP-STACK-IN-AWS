# Project 1 WEB STACK IMPLEMENTATION(LAMP STACK)IN AWS

Creating AWS account with usersname: Olanrewaju
Connecting to EC2

![Alt text](Images/Apache2.png)


 *Connecting to insance(ubuntu web server)*.

![Alt text](Images/UbuntuWeb.png)

 #### Step 1

 *Update list of packages in package manager*.

  `sudo apt update`

![Alt text](Images/sudoUpdate.png)
  
 *Run apache2 package installation*.

 `sudo apt install apache2`.

![Alt text](Images/Apache2.png)
 
 *Opened TCP PORT 80*.

 #### Step 2

 *Installing MySQL*.

  `sudo apt install mysql-server`.

![Alt text](Images/mysql-server.png)
  
  *Connecting to Mysql*

![Alt text](Images/mysqlOutput.png)
  
   *Setting password for root user using mysql_native_password*.

![Alt text](Images/ExtMysql.png)
  
   *Mysql interactive scripting*

![Alt text](Images/Mysql22.png)

 #### Step 3

    *Installing PHP*.
    
*Also installing PHP dependencies at the same time*.

 `sudo apt install php libapache2-mod-php php-mysql`.

![Alt text](Images/PHP.png)

   ![Alt text](Images/PHPversion.png)  


#### Step 4

Create directory for projectlamp

 `sudo mkdir /var/www/projectlamp`.

![Alt text](Images/projectlamp.png)


Assiging ownership of the directory

 `sudo chown -R $USER:$USER /var/www/projectlamp`.

Creating new file configuration in Apache

 `sudo vi /etc/apache2/sites-available/projectlamp.conf`.

![Alt text](Images/NewFile.png)


Enable the new virtual host

`sudo a2ensite projectlamp`.

![Alt text](Images/EnableNewVirtual.png)


Reload Apache

`sudo systemctl reload apache2`.
 
Creating an index.html file

`sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`.

#### Step 5

Changing behaviour 

`sudo vim /etc/apache2/mods-enabled/dir.conf`.

![Alt text](Images/BehaviourChange.png)


`sudo systemctl reload apache2`.

Creating new file named index.php

`vim /var/www/projectlamp/index.php`.

  ![Alt text](Images/Index.php.png)

The End





