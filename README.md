# Deploy Cloud Native Monitoring Application on Amazon Web Services (AWS)

## Prerequisites

- AWS Account
- Connect AWS Account to CLI Commands
- Python 3
- IDE – VS Code

### AWS Account
I created an AWS Account to have the possibility to deploy it.

### Connect AWS Account to CLI Commands
I created an Access Key in my AWS Account for programmatic access. Then, I opened the command line and ran the command `aws configure` to configure the CLI, copying and pasting the data obtained from the Access Key. I verified the configuration by running `aws iam list-users` to see if AWS is configured properly, confirming that the user appearing is the same as the one logged on AWS.

### Python 3
I searched for Python software and downloaded the latest version.

### IDE – VS Code
I searched for and installed Visual Studio Code.

## What Should I Work On

1. Creating a basic monitoring app with Python (Flask)
2. Create a Dockerfile
3. Create ECR using Python (Boto3)
4. Push Docker image to ECR

## Table of Modules

- [Module 1: Create Monitoring App in Flask Python](#module-1-create-monitoring-app-in-flask-python)
- [Module 2: Create Dockerfile](#module-2-create-dockerfile)
- [Module 3: Create ECR using Boto3 Python](#module-3-create-ecr-using-boto3-python)
- [Module 4: Push Docker Image to ECR](#module-4-push-docker-image-to-ecr)

## Module 1: Create Monitoring App in Flask Python

1. Create a folder and name it `Cloud_Native_Monitoring_App`.
2. Open VS Code and open the folder.
3. Create an `app.py` file and write the code for the monitoring app using Flask. Utilize the `psutil` library as needed.
4. Create a `requirements.txt` file and list the required dependencies.
5. Create an HTML file to style the app. Create a folder named `template` and create the file `index.html`.
6. Run the app using the command `python3 app.py`.

### Errors Found During the Process

I had installed the latest version of Python, so the versions of requirements didn’t fit. Therefore, I created another environment and installed Python version 3.9 directly.

## Module 2: Create Dockerfile

1. Create a file named `Dockerfile`.
2. Search for and import the correct Python image matching the installed version.
3. Write the Dockerfile to import the correct Python image.
4. In the terminal, build the Docker image using `docker build -t name-of-the-image`.
5. Check if it is working properly by running `docker images`.
6. Containerize the Docker using `docker run -p 5000:5000 image_id`.

### Errors Found During the Process

I hadn’t installed Docker software and I initially chose another image for Python at the hub due to the incorrect version. This was eventually resolved by correcting the environment and reinstalling the requirements from `requirements.txt`.

## Module 3: Create ECR using Boto3 Python

1. Create an `ecr.py` file and import `boto3`. Refer to `boto3.amazonaws.com` for correct importing.
2. Write the code to create the ECR repository.
3. Run the code in the terminal using `python3 ecr.py`.

### Errors Found During the Process

I encountered some errors while writing the code in `ecr.py`, which required rechecking the functionality with `aws configure` and `aws iam list-users`.

## Module 4: Push Docker Image to ECR

After creating the repository, use the provided "docker push commands" for Windows (since I have a Windows operating system) and copy-paste the code from the list.
