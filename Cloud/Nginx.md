## Nginx Web Server Setup and Customization

- [Nginx Web Server Setup and Customization](#nginx-web-server-setup-and-customization)
  - [Install Nginx](#install-nginx)
  - [Verify Nginx Installation](#verify-nginx-installation)
  - [Ensure Nginx is Enabled at Startup](#ensure-nginx-is-enabled-at-startup)
  - [Backup Default Nginx Webpage](#backup-default-nginx-webpage)
  - [Replace Default Nginx Webpage with Custom Content](#replace-default-nginx-webpage-with-custom-content)
  - [Download an Image and Display it on the Webpage](#download-an-image-and-display-it-on-the-webpage)


---

### Install Nginx
To install **Nginx** on the Ubuntu 18.04 LTS VM, run the following commands:

- sudo apt update
- sudo apt install nginx


### Verify Nginx Installation
- sudo systemctl status nginx

### Ensure Nginx is Enabled at Startup
- sudo systemctl is-enabled nginx

### Backup Default Nginx Webpage
- sudo mv /var/www/html/index.html /var/www/html/index.html.bak

### Replace Default Nginx Webpage with Custom Content
- create a custom index.html file. 
    - sudo nano /var/www/html/index.html
    - <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My Custom Page</title>
</head>
<body>
    <h1>Welcome to My Custom Page!</h1>
    <img src="myimage.jpg" alt="A cute cat">
</body>
</html>

### Download an Image and Display it on the Webpage
- sudo wget https://example.com/sample-image.jpg -O /var/www/html/myimage.jpg


