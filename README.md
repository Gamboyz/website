#Gameboyz Wordpress repo
Developers: Jared, Sam, Blake

#Tech
Ubuntu 14.04 LTS, Apache2, PHP-5.5.16, MySQL

#VM setup wordpress
1. make sure vm can ping and accept outside networks
- `ping google.com`
2. be in your home directory
- `cd`
3. git clone the repo from github into your user public facing folder
- `git clone https://github.com/Gameboyz/website.git ~/public_html`
4. copy over the .htaccess, fix-db-urls.php and wp-config.php files to your public_html folder
- `sudo cp /home/jared/public_html/.htaccess ~/public_html`
- `sudo cp /home/jared/public_html/fix-db-urls.php ~/public_html`
- `sudo cp /home/jared/public_html/wp-config.php ~/public_html`
5. open the .htaccess file in a text editor and replace all instances of jared with your username
6. open up phpmyadmin in your web browser on your host machine (the vm doesnt have a web browser), login as root (this info you have to request)
- `ifconfig` and find the ip address your machine is using
- `<ip_of_machine>/phpmyadmin`
7. in phpmyadmin 
    1. go to the databases tab
    2. checkmark the `wp_gameboyz` database
    3. then click the `Drop` link just below on the same page
    4. in the google drive capstone folder, download the localhost.sql file
    5. back in phpmyadmin, click on the import tab
    6. click on the browse button under File to Import and select the localhost.sql file (from where ever its stored)
    7. click go
8. go to the command line of the vm, make sure you're in the public_html directory
- `cd ~/public_html`
9. run the fix-db-urls.php script
- `./fix-db-urls.php`
10. open up your web browser and check to see if the website loads
- `<ip_of_machine>/~<username>`
12. check login for wp-admin
- `<ip_of_machine>/~<username>/wp-admin`
13. if working, good, you're done

#Using Git
##TODO

