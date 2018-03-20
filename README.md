# PHP Template App

After I needed a simple NGINX, PHP and MySQL Docker compose file I thought it is easier to put something up for quick reference for next time.

This is a great template to setup the boilerplate for a development environment. It is not complete but enough to get you started to try out some quick idea without actually installing anything on your system other than Docker.

This setup pulls in the NGINX, PHP and MySQL. The PHP image has the mysqli and pdo_mysql extensions enabled besides the default and are from my [PHP7 With Stuff](https://github.com/toomasr/php7-with-stuff) project.

To get this running just issue a `docker-compose up` in the folder. Then define the host `project.localhost` that points to 127.0.0.1 and voila, you will be presented with a **index.php** from `website/public_html/index.php` file.

# Usage

I just clone or download the repository and use it as a basis whenever I need to do some PHP prototyping (happens like once a year for me).

It runs everything on `project.localhost` URL so be sure to define that in your **hosts** file. If you want to tweak that then edit the **src/vhost.conf** file.

Everything under **website/public_html** is meant to be the **root** for the web server. The **website/lib** is left out of the served three.

The app comes with a **index.php** which just displays the [phpinfo()](http://php.net/manual/en/function.phpinfo.php).

MySql creates all its data under **db_data** folder. It also tries to load your dump files from **src/db** folder.

MySQL is set up with the root password being **mysql_root_password**. Username **mysql_username**, password being **mysql_password** and the created database **database_name**.
