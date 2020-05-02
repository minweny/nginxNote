# nginxNote

## install nginx on ubuntu
[https://www.linode.com/docs/web-servers/nginx/how-to-install-nginx-ubuntu-18-04/]  
[https://mediatemple.net/community/products/developer/204405534/install-nginx-on-ubuntu]  
[https://www.linode.com/docs/web-servers/nginx/nginx-installation-and-basic-setup/]   
[https://www.linode.com/docs/web-servers/nginx/how-to-configure-nginx/] 

```
apt-get update
apt-get install nginx
sudo /etc/init.d/nginx start
ps -ax | grep nginx

main configuration file /etc/nginx/nginx.conf, which includes
/etc/nginx/modules-enabled/*.conf - useless files
/etc/nginx/conf.d/*.conf - empty
/etc/nginx/sites-enabled/* - default, the one has the main page

the default index.html is at /var/www/test.com/
mkdir -p /var/www/example.com

Set up a new symlink to the /etc/nginx/sites-enabled/ directory to enable your configuration:
sudo ln -s /etc/nginx/sites-available/example.com /etc/nginx/sites-enabled/

Disable the default configuration file by removing the symlink in /etc/nginx/sites-enabled/:
sudo unlink /etc/nginx/sites-enabled/default

Test your configuration for errors:

sudo nginx -t
Reload the configuration:

sudo nginx -s reload
```

chromeos share file location  
/mnt/chromeos/MyFiles/  
