# Project 1
## Web Stack Implementation (LAMP Stack) in AWS
- I went to [AWS Cloud](aws.amazon.com) to create a free-tier AWS account.
- I accessed the AWS console to search for the *EC2* service and created a new instance using the launch instance wizard.
- From the wizard, I chose the *free-tier* checkbox and searched for "**Ubuntu**" to choose the 20 TLS 64bit version for creating the t2-micro instance.
- I chose the default security group, checked delete on termination, created and downloaded my key pair, and then launched the instance.
- I went to the instance list to confirm that the newly created instance is listed to be running.
- I went to the security group to edit the inbound rules of the default security group to allow access from all by changing the source to anywhere for SSH connection.
- I converted the __.pem__ file to .ppk file using PuttyGen and then used Putty to connect with the instance pulbic IP and .ppk file as the ubuntu user.
- I ran apt update and apt install apache2 to update the Ubuntu server and have Apache installed as well.
![image](https://user-images.githubusercontent.com/33117664/116108310-b585df00-a6ab-11eb-864b-373207916d21.png)
![image](https://user-images.githubusercontent.com/33117664/116108441-cfbfbd00-a6ab-11eb-9f2b-c677485f0d14.png)
![image](https://user-images.githubusercontent.com/33117664/116108693-0dbce100-a6ac-11eb-846e-747d41eedc94.png)
- I allowed port 80 in AWS security group for the HTTP protocol.
- I successfully ran the curl commands and tested the apache connectioon via a web browser using the instance public IP address.
![image](https://user-images.githubusercontent.com/33117664/116108779-21684780-a6ac-11eb-8949-d372b9254c7f.png)
![image](https://user-images.githubusercontent.com/33117664/116108869-35ac4480-a6ac-11eb-82c3-5b504f351a25.png)
- I ran apt install mysql-server to install MySQL on the instance and removed insecure settings by running the mysql script.
![image](https://user-images.githubusercontent.com/33117664/116114132-fe8c6200-a6b0-11eb-99a4-efd12beb1732.png)
![image](https://user-images.githubusercontent.com/33117664/116114296-224fa800-a6b1-11eb-9692-f5decea63bce.png)
- Afterward, I was able to run the mysql command to access the MySQL database connection.
![image](https://user-images.githubusercontent.com/33117664/116114465-4612ee00-a6b1-11eb-919c-e1ead74465a2.png)
- I ran apt install php and successfully tested with php -v command after installing PHP.
![image](https://user-images.githubusercontent.com/33117664/116114597-69d63400-a6b1-11eb-9469-9931bee5daec.png)
![image](https://user-images.githubusercontent.com/33117664/116114677-7bb7d700-a6b1-11eb-8e78-37ec19703011.png)
- Afterward, I created the **projectlamp** domain directory and assigned the _$USER_ environment variable to it.
![image](https://user-images.githubusercontent.com/33117664/116117381-13b6c000-a6b4-11eb-932e-f39595a50774.png)
![image](https://user-images.githubusercontent.com/33117664/116117749-8031bf00-a6b4-11eb-85cf-f5097a06c313.png)
- I then created the VirtualHost configuration file.
![image](https://user-images.githubusercontent.com/33117664/116118640-70ff4100-a6b5-11eb-87bf-fa0dd57d5e2e.png)
- I then used the **a2ensite** command to enable the new virtual host.
![image](https://user-images.githubusercontent.com/33117664/116119837-c425c380-a6b6-11eb-822e-e9861aaef59a.png)
- I also disabled the default site, tested the configuration and reloaded Apache for changes to take effect.
![image](https://user-images.githubusercontent.com/33117664/116120076-10710380-a6b7-11eb-80ce-721fea87b4f5.png)
- Finally, I created an *index.html* page with contents for the site to test.
![image](https://user-images.githubusercontent.com/33117664/116120515-84aba700-a6b7-11eb-82fb-5ffd1dc6227f.png)
- Afterward, I enabled PHP on the webiste by disabling the defualt behaviour of the index.html file.
![image](https://user-images.githubusercontent.com/33117664/116121222-511d4c80-a6b8-11eb-877d-7abcee73b5ed.png)
- I then created a new index.php file to test this.
![image](https://user-images.githubusercontent.com/33117664/116121445-84f87200-a6b8-11eb-82b1-4e78a6f56b60.png)
- After successfully testing, I deleted the php file.
![image](https://user-images.githubusercontent.com/33117664/116121681-c6891d00-a6b8-11eb-96b8-75c321bd24cd.png)







