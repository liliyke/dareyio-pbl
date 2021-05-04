# Project 2
## Web Stack Implementation (LEMP Stack)
- I went to [AWS Cloud](aws.amazon.com) to create a free-tier AWS account.
- I accessed the AWS console to search for the *EC2* service and created a new instance using the launch instance wizard.
- From the wizard, I chose the *free-tier* checkbox and searched for "**Ubuntu**" to choose the 20 TLS 64bit version for creating the t2-micro instance.
- I chose the default security group, checked delete on termination, used my existing key pair, and then launched the instance.
- I went to the instance list to confirm that the newly created instance is listed to be running.
- I went to the security group to edit the inbound rules of the default security group to allow access from all by changing the source to anywhere for SSH connection.
- I launched *GitBash* and used the __.pem__ file to connect with the instance pulbic IP as the ubuntu user.
![image](https://user-images.githubusercontent.com/33117664/116296257-e8a29e00-a791-11eb-8a82-fbc3cbaa89ca.png)
- I ran apt update and apt install nginx to update the Ubuntu server and have Nginx installed as well.
![image](https://user-images.githubusercontent.com/33117664/116297508-3c61b700-a793-11eb-9032-e0e5404fb2e5.png)
![image](https://user-images.githubusercontent.com/33117664/116304405-72ef0000-a79a-11eb-8872-0d6369cf219b.png)
![image](https://user-images.githubusercontent.com/33117664/116304666-b9dcf580-a79a-11eb-88ea-95865d0c6667.png)
- I allowed *port 80* in AWS security group for the HTTP protocol.
- I successfully ran the curl commands and tested the apache connectioon via a web browser using the instance public IP address.
![image](https://user-images.githubusercontent.com/33117664/116304891-f4469280-a79a-11eb-993c-e7f69881f8fb.png)
![image](https://user-images.githubusercontent.com/33117664/116304955-058f9f00-a79b-11eb-8abd-0b3d2207858c.png)
- I ran apt install mysql-server to install MySQL on the instance and removed insecure settings by running the mysql script.
![image](https://user-images.githubusercontent.com/33117664/116305509-c9107300-a79b-11eb-8f83-329e94e23f5c.png)
![image](https://user-images.githubusercontent.com/33117664/116305671-ffe68900-a79b-11eb-943f-0a0b20c8552f.png)
- Afterward, I was able to run the mysql command to access the MySQL database connection.
![image](https://user-images.githubusercontent.com/33117664/116305804-302e2780-a79c-11eb-9ada-561865720a65.png)
- I ran apt install php-fpm and php-mysql to successfully install PHP.
![image](https://user-images.githubusercontent.com/33117664/116308123-0b877f00-a79f-11eb-8cf6-0b51e976042f.png)
- I configured Nginx to use PHP Processor and restarted the service.
![image](https://user-images.githubusercontent.com/33117664/116310200-99646980-a7a1-11eb-8bcc-a6ac90b05942.png)
- Finally, I created an *index.html* page with contents for the site to test.
![image](https://user-images.githubusercontent.com/33117664/116310687-3de6ab80-a7a2-11eb-8bdb-ed0b3727571c.png)
- I successfully tested PHP with Nginx.
![image](https://user-images.githubusercontent.com/33117664/116311347-1217f580-a7a3-11eb-96eb-cbee2def0dc2.png)
