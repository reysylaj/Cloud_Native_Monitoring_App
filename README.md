**DEPLOY CLOUD NATIVE MONITORING APPLICATION ON AMAZON WEB SERVICE**

<br>

**PREREQUISITIES**
1.	AWS Account
2.	Connect AWS Account to CLI Commands
3.	Python3
4.	IDE – VS Code

- AWS Account
I created an AWS Account to have the possibility to deploy it.

- Connect AWS Account to CLI Commands
I created an Access Key at my AWS Account for programmatic access.
Opened cmd and ran: aws configure and copy-paste the data obtained from the Access Key.
I ran: aws iam list-users to see if aws is configurated properly and see that the user that is appers is the same with the account logged on AWS.

- Python3
I searched for Python software and downloaded the last version.

- IDE – VS Code
Searched and installed Visual Studio Code.


<br>

**WHAT SHOULD I WORK ON**
1.	Creating a basic monitoring app with Python (Flask)
2.	Create a Dockerfile
3.	Create ECR using Python (Boto3)
4.	Push Docker image to ECR


<br>

**TABLE OF MODULES**
Module 1: CREATE MONITORING APP IN FLASK PYTHON	4
Module 2: CREATE DOCKERFILE	5
Module 4: PUSH DOCKER IMAGE TO ECR	7


<br>


**Module 1: CREATE MONITORING APP IN FLASK PYTHON**

Firstly, I created a folder and named: Cloud_Native_Monitoring_App
Open VS Code and opened the folder.
Created an app.py file and write the code of the monitoring app.
I worked with psutil, so I imported the library correctly.

Secondly, I created another file requiriments.txt and wrote the requirements to be installed

Thirdly I created a html file to style the app.
I created a folder template and created the file index.html and wrote the code of the code of the style.

Finally, I ran the code: python3 app.py to run the app.

ERRORS FOUND DURING THE PROCESS:
I had installed the latest version of python so the versions of requirements didn’t fit. So I created another environment and installed directly the python version 3.9.

<br>



**Module 2: CREATE DOCKERFILE**

Firstly, I created a file named Dockerfile, and after I searched on google to import the correct image of the python that I have installed.
In Dockerfile I wrote the code to import the right image.

Secondly. in terminal I created the image of Dockerfile: docker build -t name-of-the-image.
To check if it is working properly, run: docker images 

Thirdly, containerize the docker: docker run -p 5000:5000 image_id .


ERRORS FOUND DURING THE PROCESS:
I haven’t installed Docker software and I chose another image to run at hub for Python, because of the incorrect version, that I eventually changed with correcting the environment and reinstalling the requirements from requirements.txt.


<br>



**Module 3: CREATE ECR USING BOTO3 PYTHON**

Firstly, I created an ecr.py file and import boto3
To import it correctly, I visited: boto3.amazonaws.com

Secondly, I wrote the code and run the code at terminal: python3 ecr.py
This way the repository is created successfully at AWS account.


ERRORS FOUND DURING THE PROCESS:
I received some errors in writing the code at ecr.py, so I had to check again the functionality with aws configure, and aws iam list-users.


<br>



**Module 4: PUSH DOCKER IMAGE TO ECR**

At the repository created, there is “docker push commands” for windows (since I have a windows operating system) and I copy pasted the code from the list.
