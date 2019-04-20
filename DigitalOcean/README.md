#DigitalOcean:

### Ubuntu Linux

- Update Ubuntu
```bash
apt-get update && apt-get upgrade
```

#### Static Web Setup

- Create New Website: example.com

```bash
sudo mkdir -p /var/www/example.com/public_html
```

- Set Permission

```bash
sudo chown -R $USER:$USER /var/www/example.com/public_html
```

- Configure Apache Virtual Hosts
- Copy default coniguration to new one.
```bash
sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/example.com.conf
```

- Edit config and match the folder location

```bash
sudo nano /etc/apache2/sites-available/example.com.conf
```

- Enable the New website

```bash
sudo a2ensite example.com.conf
```

- Create new HTML and test everything is working fine

```bash
nano /var/www/example.com/public_html/index.html
```

- Restart the Apache

```bash
sudo systemctl restart apache2
```

- Visit web : example.com

#### WordPress Setup
- Upload files via WinSCP/ Filezilla e.g. WordPress.zip
- Extract it via commandline

```bash
unzip /var/www/example.com/public_html/wordpress.zip
```

- Move file to web root if need e.g. /var/www/example.com/public_html

#### MySQL Setup

- Login to MySQL DB

```bash
mysql -u root -p
```

- Create DB

```bash
CREATE DATABASE exampledb;
```

- Create User

```bash
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
```

- Assign Permission

```bash
GRANT ALL PRIVILEGES ON * . * TO 'username'@'localhost';
```

- Install WordPress via visiting : example.com
    - username
    - password
    - exampledb

- WordPress Plugin Install FTP details required Issue Resolve

```bash
chown -Rf www-data.www-data /var/www/example.com/public_html
```




