## Nginx Web Server Setup and Customization: 

- [Nginx Web Server Setup and Customization:](#nginx-web-server-setup-and-customization)
  - [](#)
  - [Install Nginx (webserver); serves web pages:](#install-nginx-webserver-serves-web-pages)
  - [Verify Nginx Installation](#verify-nginx-installation)
  - [Ensure Nginx is Enabled at Startup](#ensure-nginx-is-enabled-at-startup)
  - [Backup Default Nginx Webpage](#backup-default-nginx-webpage)
  - [Replace Default Nginx Webpage with Custom Content](#replace-default-nginx-webpage-with-custom-content)
  - [Download an Image and Display it on the Webpage](#download-an-image-and-display-it-on-the-webpage)
  - [Use the Public IP address to access the webpage. (http://.....)](#use-the-public-ip-address-to-access-the-webpage-http)


---


### 

- sudo apt update -y
- sudo apt upgrade -y 

### Install Nginx (webserver); serves web pages: 
To install **Nginx**, run the following commands:
```bash
- nano provision.sh
```
- Add these to the file:
```bash
# update 
sudo apt update -y
# upgrade
sudo apt upgrade -y
 ## check if it ask for user input; if it does it will hang waiting for user input. 

 ## ctrl +s , Ctrl +x 

# install nginx
sudo apt install nginx -y

- must restart to take effect of changes

# restart nginx
sudo systemctl restart nginx

# enable nginx
sudo systemctl enable nginx

```
- check public IP for the VM and then it should work; http://


```
- sudo apt-get update -y
- sudo apt install nginx
    - super user do "root user"


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
- or use curl https:// ...... --output cat.jpg
- using wget requires elevated permission so sudo might be needed compared to using curl.
  
### Use the Public IP address to access the webpage. (http://.....) 
