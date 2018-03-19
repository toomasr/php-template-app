# PHP Template App

After I needed a simple NGINX, PHP and MySQL Docker compose file I thought it is easier to put something up fro quick reference next time.

This is a great template to setup the boilerplate for a development environment. It is not complete but enough to get you started to try out some quick idea without actually installing anything on your system other than Docker.

This setup pulls in the NGINX, PHP and MySQL. The PHP image has the mysqli and pdo_mysql extensions enabled besides the default.

# Usage

I just clone or download the repository and use it as a basis whenever I need to do some PHP prototyping (happens like once a year for me).

It runs everything on `project.localhost` URL so be sure to define that in your *hosts* file. If you want to tweak that then edit the *src/vhost.conf* file.

Everything under *website/public_html* is meant to be the *root* for the web server. The *website/lib* is left out of the served three.

The app comes with a *index.php* which just displays the [phpinfo()](http://php.net/manual/en/function.phpinfo.php).

MySql creates all its data under *db_data* folder. It also tries to load your dump files from *src/db* folder.

MySQL is set up with the root password being *mysql_root_password*. Username *mysql_username*, password being *mysql_password* and the created database *database_name*.
