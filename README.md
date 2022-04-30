# steps to install nopcommerce
Updating  all packages

Install unzip package 

Download Microsoft package

Install ASP.NET runtime

install Nginx and configure it

Once the installation is complete, we will delete the default server blocks and configure a new one for nopCommerce the comands are below

sudo rm -rf /etc/nginx/sites-available/default

sudo rm -rf /etc/nginx/sites-enabled/default

Configure Nginx for nopCommerce

sudo nano /etc/nginx/sites-available/nopcommerce.conf

Enable the configuration by creating a symlink to sites-enabled directory

sudo ln -s /etc/nginx/sites-available/nopcommerce.conf /etc/nginx/sites-enabled/nopcommerce.conf

Restart Nginx

Install nopCommerce

cd /var/www/html

download the url and extract it sudo wget https://github.com/nopSolutions/nopCommerce/releases/download/release-4.50.1/nopCommerce_4.50.1_NoSource_linux_x64.zip

Extract the downloaded file.

Configure nopCommerce as a Service

Create a new service file.

sudo nano /etc/systemd/system/nopcommerce.service

sudo systemctl daemon-reload

Enable nopCommerce to start at system boot.

Start nopCommerce.

Check status using the following command.


