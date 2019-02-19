**This EC2 bootstrap script will updates the yum repository, insalls httpd server, creates a html file, starts the httpd server and updates configuration to set httpd as a service**

````bash
#!/bin/bash
yum update -y
yum install httpd -y
cd /var/www/html
echo "Web Server 1 - Ireland" > index.html
service httpd start
chkconfig httpd on
````

