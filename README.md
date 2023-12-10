## IDS 706 Individual Project 4: Auto Scaling Flask App Using Any Serverless Platform

This repository is for IDS706 Individual Project 4: Auto Scaling Flask App Using Any Serverless Platform

## Video Demo
Video Demo can be found in : [individual project 4 demo video youtube]()

## Key Functions

**Building Schedule**
This designed Flask app helps to build schedule for target consumer according to their daily tasks and to-dos. The consumer will input their daily tasks in the command line. These tasks will then be organized into a designed daily schedule that helps them organize their to-dos. 

## APP Demonstration
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

## Github actions
Status badges for CI.yml
`CI.yml`
[![CI](https://github.com/nogibjj/Individual_Project4_Kelly_Tong/actions/workflows/CI.yml/badge.svg)](https://github.com/nogibjj/Individual_Project4_Kelly_Tong/actions/workflows/CI.yml)



## Preparation and Setup
1. clone the repository
2. modify requirements.txt file to contain the necessary packages
3. use `pip install Flask` to install Flask on codespace
4. login to Azure
5. Create an account with Docker Hub and prepare a repository for storing images
   
<img width="1356" alt="截屏2023-12-09 21 04 05" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/8e2576b6-d887-4db1-a2c9-28d7b0f64e88">

6. Create an App on Azure using App service and Web App, remember to set Publish to Docker Container and Image Source to Docker Hub
<img width="1372" alt="截屏2023-12-09 21 06 00" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/80d1b03d-29c5-4735-a059-5b2a63722c39">


7. Add a configuration of Website_Port = 5000 in Configuration under Setting
   <img width="613" alt="截屏2023-12-09 21 07 47" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/6df8092d-2e85-4a88-bdc9-e381f7eb6768">

8. Use the Flask App as demonstrated in App usage below

## App Usage
1. Click plan your day
2. Input the daily to-dos
   
<img width="1400" alt="截屏2023-12-09 21 12 28" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/94ac597d-ac44-4cfc-bf30-ea24928429b0">

3. Click Generate Schedule
4. A Planned schedule will be shown
<img width="1222" alt="截屏2023-12-09 21 12 36" src="https://github.com/nogibjj/Individual_Project4_Kelly_Tong/assets/142815940/591d5fea-9cac-4b98-a344-2c25560bbc2c">


