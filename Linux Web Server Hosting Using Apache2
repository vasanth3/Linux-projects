# Linux Web Server Hosting Using Apache2

## Project Overview

This project demonstrates how to host a website on Ubuntu Linux using the Apache2 web server.

The website is developed using HTML and CSS and hosted on a Linux server. This project covers basic web server installation, configuration, website deployment, and file permissions.

## Technologies Used

- Ubuntu Linux 24.04 LTS
- Apache2 Web Server
- HTML5
- CSS3
- Linux Commands

## Project Structure

```text
linux-web-hosting/
├── index.html
├── style.css
└── README.md
```

## Project Implementation

### 1. Install Apache2

Update the package repository and install Apache2.

```bash
sudo apt update
sudo apt install apache2 -y
```

### 2. Start Apache2

Start and enable the Apache2 service.

```bash
sudo systemctl start apache2
sudo systemctl enable apache2
```

### 3. Create Website Directory

Create the website directory.

```bash
sudo mkdir -p /var/www/html
```

### 4. Deploy Website Files

Open the Nano file editor and create the HTML and CSS files in the Apache website directory.

Create the HTML file:

```bash
sudo nano /var/www/html/index.html
```

Create the CSS file:

```bash
sudo nano /var/www/html/style.css
```

### 5. Configure Permissions

Check the Apache2 processes.

```bash
ps aux | grep apache2
```

This command is used to check the Apache2 processes. On Ubuntu, Apache2 normally uses `www-data` as its worker user.

Set the ownership to `www-data`.

```bash
sudo chown -R www-data:www-data /var/www/html
```

### 6. Set Directory and File Permissions

Set directory permissions to 755 and file permissions to 644.

```bash
sudo find /var/www/html -type d -exec chmod 755 {} \;
sudo find /var/www/html -type f -exec chmod 644 {} \;
```

### 7. Apache2 Configuration File

Create the Apache2 configuration file.

```bash
sudo nano /etc/apache2/sites-available/mysite.conf
```

Add the following configuration.

```apache
<VirtualHost *:80>

    ServerName localhost

    DocumentRoot /var/www/html

    <Directory /var/www/html>
        Options -Indexes
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/mysite_error.log
    CustomLog ${APACHE_LOG_DIR}/mysite_access.log combined

</VirtualHost>
```

#### Enable the Website

```bash
sudo a2ensite mysite.conf
```

#### Check Apache2 Configuration

Run the following command to check the Apache2 configuration.

```bash
sudo apache2ctl configtest
```

Expected output:

```text
Syntax OK
```

#### Reload Apache2

```bash
sudo systemctl reload apache2
```

Check the Apache2 service status.

```bash
sudo systemctl status apache2
```

### 8. Access the Website

Open a web browser and enter the server IP address.

```text
http://YOUR_SERVER_IP
```

The website should now be accessible through the server IP address.

## Skills Learned

- Linux server administration
- Apache2 installation and configuration
- HTML and CSS website development
- Linux file permissions and ownership
- Web server troubleshooting
- Website deployment
- Apache2 VirtualHost configuration
- Linux service management

## Conclusion

This project helped me understand the fundamentals of Linux web hosting and Apache2 configuration. It provided practical experience in deploying a website on an Ubuntu Linux server, managing file permissions, and configuring a web server to serve a custom website.

This project is part of my hands-on Linux system administration learning journey.
