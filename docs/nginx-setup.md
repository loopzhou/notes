# Install Nginx

## install

```bash
sudo apt-get update
sudo apt-get install nginx
```

## Manage the Nginx Process

```bash
sudo systemctl stop nginx  #停止

sudo systemctl start nginx

sudo systemctl restart nginx

sudo systemctl reload nginx #重新加载配置
```

/usr/share/nginx/html

## Server Directory

### Content

- ```/var/www/html```: The actual web content, which by default only consists of the default Nginx page you saw earlier, is served out of the /var/www/html directory. This can be changed by altering Nginx configuration files.

### Server Configuration

- ```/etc/nginx```: The Nginx configuration directory. All of the Nginx configuration files reside here.
- ```/etc/nginx/nginx.conf```: The main Nginx configuration file. This can be modified to make changes to the Nginx global configuration.
- ```/etc/nginx/sites-available/```: The directory where per-site "server blocks" can be stored. Nginx will not use the configuration files found in this directory unless they are linked to the sites-enabled directory (see below). Typically, all server block configuration is done in this directory, and then enabled by linking to the other directory.
- ```/etc/nginx/sites-enabled/```: The directory where enabled per-site "server blocks" are stored. Typically, these are created by linking to configuration files found in the sites-available directory.
- ```/etc/nginx/snippets```: This directory contains configuration fragments that can be included elsewhere in the Nginx configuration. Potentially repeatable configuration segments are good candidates for refactoring into snippets.

### Server Logs

- ```/var/log/nginx/access.log```: Every request to your web server is recorded in this log file unless Nginx is configured to do otherwise.
- ```/var/log/nginx/error.log```: Any Nginx errors will be recorded in this log.

## Reference

- <https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-16-04>
- <https://www.cnblogs.com/zhouxinfei/p/7862285.html>
