![image](https://github.com/user-attachments/assets/133d1c07-2aaa-407c-be8e-86d3ad6acdf1)# Details of the web app

## Step 1: Provisioning the Server

search for EC2 on the search box.
![image](https://github.com/user-attachments/assets/47ecfa54-add9-4f66-a0fa-cca7a2c66677)

click on the EC2 
![image](https://github.com/user-attachments/assets/8a2fc3b6-8d99-4b79-a783-97802e6400db)

click to instance to create/lunch an instance

![image](https://github.com/user-attachments/assets/81cd9c1c-9795-42ff-bcab-09fb187fb79f)

click on lunch an instance 
![image](https://github.com/user-attachments/assets/3eaa9496-eefe-447e-b07b-0dcf7d6a1478)

### Now start create an OS image by picking an preferable one.
In my case i will pick ***UBUNTU*** with the steps below:

1. Choose a name and tag.
   ![image](https://github.com/user-attachments/assets/47cd9f85-121d-4d2f-a293-18383b7fd73b)

2. choose Application and OS Images.
  ![image](https://github.com/user-attachments/assets/81456476-dbbc-490a-93a6-75e0008fbaca)

3. choose the machine IMage of preference.
 ![image](https://github.com/user-attachments/assets/e6de7977-8bda-4957-aeec-7080181167d3)

4. select a key pair name if you already have or create a new one
 ![image](https://github.com/user-attachments/assets/3b64e574-101f-4254-b295-e8601bff3fbb)

5. choose configure storage.
   ![image](https://github.com/user-attachments/assets/399075e5-8b89-4777-8e9f-a07c260a033a)

6. Leave the other configuration to default and click on lunch ***instance***
   ![image](https://github.com/user-attachments/assets/e5534c48-f44c-42cd-8cea-116a3661be06)

   A result of this will pop up after clicking the lunch instance.
   ![image](https://github.com/user-attachments/assets/e0411a5c-cbd2-4c2c-9285-26b032104714)

   Now the instance is up and running.
   ![image](https://github.com/user-attachments/assets/15a45fe3-e3fb-4d88-8045-0d93c950e0b0)

  
## Step 2: Web Server Setup.
###  Installing a web server (e.g., Apache, Nginx) to serve web content.

Connecting to server first:

click on the box to bring out the instance info.
![image](https://github.com/user-attachments/assets/0a5fbd26-01d8-4f9d-9ef1-f93e9ef3442e)

click on ***connect*** or click on the arrow beside ***action*** and click connect
![image](https://github.com/user-attachments/assets/cf36b642-c1c5-4d76-805d-0f808e53b617)

connect to instance using any preferable option, but for my case i will pick ***SSH CLIENT***

![image](https://github.com/user-attachments/assets/2d570f83-4596-4d3e-852f-bf62990e4364)

#### Open a ***Terminal*** of your choice.

click on the link where an arrow pointed to which contain a pair key of the instance and paste on the terminal.
![image](https://github.com/user-attachments/assets/4a339deb-dd4e-4e2c-b5ec-2987195e0281)

A result like this will pop up if definitely doing the right thing.
![image](https://github.com/user-attachments/assets/463121da-2d9c-412f-832d-71ba1e84b90d)

Follow the instruction on the terminal for successful connection. you will get the below result.
![image](https://github.com/user-attachments/assets/1e028042-019a-4e37-8ed2-5a2a7cbc80d2)

### Installing Apache server.
#### Steps to install Apache server.
1. Change to Superuser which is root with ***sudo su***
   
![image](https://github.com/user-attachments/assets/34d2284e-eda6-4c6e-8dfe-4850ec4af7bc)

2. Update Ubuntu package with ***sudo apt update***
![image](https://github.com/user-attachments/assets/a653b80a-14b8-4ff2-b32e-b6128ffdf304)

3. Install Apache on the machine with ***sudo apt install apache2***
![image](https://github.com/user-attachments/assets/b93cb4be-1578-4e28-9876-0083ceb2567b)

4. After installing the Apache server automatically start check the status with ***sudo systemctl status apache2***
   ![image](https://github.com/user-attachments/assets/be5c5a1a-d03c-49e8-b074-96ec730b535c)

## Step 3 Web Content Page Deployment.
### Deployin the Web Content on the server.
1. Create a directory and name it ***temp*** with ***mkdir temp***.
2. Change to the ***temp*** directory with ***cd temp***
3. Get the link on the site you want to host and download it with ***wget https://github.com/Hollumidhe/ALT-schoool-second-semester-exam*** (i hosted mine on git)
4. Check if all the files are  available with ***ls -lrt***
5. Change the location.
6. Move all the files to this location ***/var/www/html/*** with mv */var/www/html/

## Step 4 Networking.
### Configure the server to allow HTTP traffic (port 80).
#### Steps on how to open HTTP trafic port
1. Check the status of your firewall with ***ufw status verbose***
![image](https://github.com/user-attachments/assets/5aad338e-fa22-4df7-9844-5d5ef5653e66)

2. check if there are any rules added to it with ***sudo ufw show added***
![image](https://github.com/user-attachments/assets/c29c3d09-642d-4384-8f79-05836723fb63)

3. Activate it since its inactive with ***sudo ufw enable*** you will get this after accepting yes.
![image](https://github.com/user-attachments/assets/f0383a03-c79c-4917-af46-c3bc4f3ef6ce)

4. 















