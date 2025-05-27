Instalar
===

Pre-requisito: LAMP


```bash
# Require laravel installer globally.
composer global require laravel/installer 

# Update your system's PATH on Ubuntu after installing the Laravel installer globally via Composer.
#1. Find the Composer bin directory:
~/.config/composer/vendor/bin or ~/.composer/vendor/bin.

#2. Update your system's PATH:
vim ~/.bashrc
- Add the following line at the end of the file (replace the path if necessary):
export PATH="$PATH:$HOME/.config/composer/vendor/bin"

#3. Apply the changes:
source ~/.bashrc

# Command to fix deppendency issues
sudo apt-get install php8.4-xml 
sudo apt install php-sqlite3

# Enable sqlite extension in php.ini
extension=pdo_sqlite
extension=sqlite3


# Create a new project.
$ laravel new laravelsite

# fix permission issues
sudo chown -R $USER:www-data /var/www/html/laravelsite/storage
sudo chown -R $USER:www-data /var/www/html/laravelsite/bootstrap/cache
sudo chmod -R 775 /var/www/html/laravelsite/storage
sudo chmod -R 775 /var/www/html/laravelsite/bootstrap/cache

sudo chown www-data:www-data /var/www/html/laravelsite/database/database.sqlite
sudo chmod 664 /var/www/html/laravelsite/database/database.sqlite
sudo chown -R www-data:www-data /var/www/html/laravelsite/database
sudo chmod -R 775 /var/www/html/laravelsite/database

sudo service apache2 restart
```


