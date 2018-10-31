https://laravel.com/docs/5.7/installation

***how to build the enviroment of php7 in linux***

sudo apt-get install php7.0-cli 	//install php7
php --version 						//check the version
php -m 								//check the modole
sudo apt-get install php-mbstring 	//install modole of mbstring
sudo apt-get install php-xml		//install modole of xml

***to install laravel, we need another program called COMPOSER, so we must install COMPOSER FIRST***

php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('SHA384', 'composer-setup.php') === '93b54496392c062774670ac18b134c3b3a95e5a5e5c8f1a9f115f203b75bf9a129d5daa8ba6a13e2cc8a1da0806388a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"

***now install laravel***
php composer.phar global require "laravel/installer=~1.1"

//Make sure to place composer's system-wide vendor bin directory in your $PATH so the laravel executable can be located by your system. This directory exists in different locations based on your operating system; however, some common locations include:
//GNU / Linux Distributions: $HOME/.config/composer/vendor/bin
***install apache in linux***
sudo apt-get install apache2

***create laravel project in var/www/html***
//but we need to change the mode in /var/www/html
sudo chmod -R 777 /var/www/html
php composer.phar create-project --prefer-dist laravel/laravel /var/www/html/my_laravel

[error]:php 7 Mcrypt PHP extension required
sudo apt-get update
sudo apt-get install mcrypt php7.0-mcrypt
sudo apt-get upgrade

sudo service apache2 restart
