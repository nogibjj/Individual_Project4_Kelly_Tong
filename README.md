## IDS 706 Individual Project 4: Auto Scaling Flask App Using Any Serverless Platform

This repository is for IDS706 Individual Project 4: Auto Scaling Flask App Using Any Serverless Platform

## Purpose
The purpose of this repository is to demonstrate the process for creating a Flask app via Azure web app service. The Flask app has its self designed functionality. In this case, it is designed to build a daily schedule for an incoming audience. Input the daily to-dos and the schedule builder will build your schedule based on a daily time schedule. Docker is used in this repository to contain image. 

## Video Demo
Video Demo can be found in : [individual project 4 demo video youtube]()

## Key Functions

**Building Schedule**
This designed Flask app helps to build schedule for target consumer according to their daily tasks and to-dos. The consumer will input their daily tasks in the command line. These tasks will then be organized into a designed daily schedule that helps them organize their to-dos. 

## APP Demonstration
APP can be found here: [ScheduleBuilder](http://myfinalschedule.kindground-9784b48c.westus2.azurecontainerapps.io)
<img width="1262" alt="截屏2023-12-09 21 01 48" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/8e27f88e-353a-44f5-a014-c0d0a5f1c063">

    
## Important Things included are:
- ``.devcontainer`` includes a Dockerfile and devcontainer.json.
                The 'Dockerfile' within this folder specifies how the container should be built

- ``workflows`` includes CI.yml, which contain configuration files for setting up automated build, test, and deployment pipelines

- ``.gitignore`` is used to specify which files or directories should be excluded from version control when using Git.

- ``Makefile`` is a configuration file used in Unix-based systems for automating tasks and building software. It contains instructions and dependencies for compiling code, running tests, and other development tasks.

- ``README.md`` is the instruction file for the readers.

- ``main.py`` is a Python file. This specific main.py gets the python versions and operation system names. 

- ``requirements.txt`` is to specify the dependencies (libraries and packages) required to run the project.

- ``test_main.py`` is a test file for main.py

- ``templates`` folder includes all the templates for the app
  
- ``static`` includes the necessary files which are downloadede
  
- ``Dockerfile``is provided to containerize the Flask app

## Github actions
Status badges for CI.yml
`CI.yml`
[![CI](https://github.com/nogibjj/Individual_Project4_Kelly_Tong/actions/workflows/CI.yml/badge.svg)](https://github.com/nogibjj/Individual_Project4_Kelly_Tong/actions/workflows/CI.yml)

## Preparation and Setup
1. clone the repository
2. modify requirements.txt file to contain the necessary packages
3. use `pip install Flask` to install Flask on codespace
4. use `brew update && brew install azure-cli` to install azure-cli locally
5. login to Azure locally using "az login"
6. Build an image locally using `docker build --tag myfinalschedule .`
<img width="882" alt="截屏2023-12-10 13 24 45" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/69b0a2ad-5235-42a9-acf0-ce7ab18baaf5">
   
7. Build a container locally using `docker run --detach --publish 5000:50505 myfinalschedule`
   
<img width="813" alt="截屏2023-12-10 13 23 46" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/3cefbe70-78f2-411a-94c5-f628336ad08b">

8. Create an App on Azure using `az containerapp up --resource-group myfinalschedule --name myfinalschedule --ingress external --target-port 50505 --source .` This will first create the resource group, run the same line again to create the flask app.
   
<img width="1141" alt="截屏2023-12-10 13 27 10" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/8e25f88f-a7e4-4a2c-a759-d0ae1fca894f">

<img width="1395" alt="myfinalschedule" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/1ecf7aae-4e4b-4b94-a0b5-1dd72205dc6e">


10. Set API_TOKEN in environment variable 
11. Use the Flask App as demonstrated in App usage below
12. App can be viewed in Azure Container and image can be viewed in container registry which are both in Azure Web Portal

## App Usage
1. Click plan your day
2. Input the daily to-dos
   
<img width="1400" alt="截屏2023-12-09 21 12 28" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/94ac597d-ac44-4cfc-bf30-ea24928429b0">

3. Click Generate Schedule
4. A Planned schedule will be shown
<img width="1222" alt="截屏2023-12-09 21 12 36" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/591d5fea-9cac-4b98-a344-2c25560bbc2c">

## Docker and Azure Container APP Registry
Image Storage: The image "myfinalschedule" is stored in Azure APP Registry. It is automatically stored when the command line `az containerapp up --resource-group myfinalschedule --name myfinalschedule --ingress external --target-port 50505 --source .` is run for the second time. 

<img width="1256" alt="截屏2023-12-10 13 34 56" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/a18f81eb-42d7-4ed7-bee8-a17dcf994275">

