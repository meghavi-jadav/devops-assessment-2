# devops-assessment-2
### Set up a simple web server using Nginx on a Linux VM. Ensure it serves a basic HTML page.

###  Update Package list

```bash
sudo apt update
```
 It updates the list of available packages and their versions from the software repositories configured on your system.
- sudo: Grants administrative (superuser) privileges to run the command.
- apt: Refers to the package manager.
- update: Tells apt to refresh its package database.

![image](https://github.com/user-attachments/assets/702e96a8-c5cd-4b57-8202-1ca42dfd5e5e)

### Install Nginx

```bash
sudo apt install nginx -y
```
This installs the Nginx web server package on your system.
- The -y flag automatically answers "yes" to any prompts during installation.

### Enable nginx at boot

```bash
sudo systemctl enable nginx
```
This ensures that the Nginx service starts automatically whenever your system reboots.
- systemctl: A command-line tool used to manage system services in Linux (services, processes, and system units).
- enable: Tells systemctl to configure Nginx to automatically start at boot.

![image](https://github.com/user-attachments/assets/52a6ee03-5033-48a4-a43d-bbdc2e4d8fc8)

### Test nginx configuration 

```bash
sudo nginx -t
```
This command tests the Nginx configuration for syntax errors or other issues.
- If there are errors in your Nginx configuration file (/etc/nginx/nginx.conf), it will let you know. If everything is fine, it will report "syntax is ok" and "test is successful". This is a useful step whenever you make changes to the Nginx configuration to ensure it will run correctly.

### Start nginx service

```bash
sudo systemctl start nginx
```

 This command starts the Nginx service if it isn’t running already.
- If you’ve made configuration changes and tested them with nginx -t, this will apply the changes by starting (or restarting) the service.
![image](https://github.com/user-attachments/assets/e2700a25-5145-42d0-8036-3829d21ddcd3)

### Check nginx status

```bash
sudo systemctl status nginx
```
The command sudo systemctl status nginx is used to check the current status of the Nginx service on your system
![image](https://github.com/user-attachments/assets/943c7818-6ffd-497b-816e-ea6d4cbbbc15)

### Create the HTML page
```bash
sudo nano /var/www/html/index.html
```
![image](https://github.com/user-attachments/assets/5b242962-14ec-404e-946d-b72f0aec228c)

### View the page on the web browser
![image](https://github.com/user-attachments/assets/b54c6c77-18b9-4974-90d4-7b079227546c)

### Stop the nginx service

```bash
sudo systemctl stop nginx
```

![image](https://github.com/user-attachments/assets/d07864d3-b6ea-4ab6-a555-a2e494ab79c9)


