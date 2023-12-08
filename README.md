# IDS 706 Individual Project 4: Auto Scaling Flask App Using Any Serverless Platform

This repository is for IDS706 Individual Project 4: Auto Scaling Flask App Using Any Serverless Platform

## Video Demo
Video Demo can be found in : [individual project 4 demo video youtube]()

## Purpose 

    
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

- ``setup.py`` setup the local packages for python, specify the dependencies required in the package. This executes the ETL streamline commands which can be called by a Makefile commnd. 

- ``mylib`` includes ``extract.py`` ``transform_load.py`` and ``query_viz.py`` which are used to extract
  a csv from an url, clean it and return a db file.

- ``run_job.py`` is included in a makefile command ``Makefile`` and in ``CI.yml`` to perform automatic run of the databrick job when Github Action is triggered through push. 

## Github actions
Status badges for CI.yml
`CI.yml`
[![CI](https://github.com/nogibjj/Individual_Project3_Kelly_Tong/actions/workflows/CI.yml/badge.svg)](https://github.com/nogibjj/Individual_Project3_Kelly_Tong/actions/workflows/CI.yml)

## Key Functions

**Building Schedule**
This designed Flask app helps to build schedule for target consumer according to their daily tasks and to-dos. The consumer will input their daily tasks in the command line. 

## Preparation
**1. Establish a Databricks Workspace:**
    Initiate a Databricks workspace within a cloud environment, such as Azure, to leverage its data processing and analytics capabilities.

**2. GitHub Integration:**
    Link your GitHub account with the Databricks Workspace to facilitate seamless code management and version control.

    
<img width="795" alt="Link Account Databrick" src="https://github.com/nogibjj/Individual_Project3_Kelly_Tong/assets/142815940/cf3aea9d-2b40-4f15-a564-2ccbbde29db6">

    
**3. Initialization Script Setup:**
    In your Databricks cluster, implement a global initialization script. This script should define necessary environment variables, ensuring a consistent runtime environment.

**4. Cluster Configuration for PySpark:**
    Configure and activate a Databricks cluster that is optimized for running PySpark applications, enabling efficient processing of large-scale data with Spark and Python.

**5. Repository Cloning:**
    Directly clone your project’s repository into the Databricks workspace. This step brings your codebase into the Databricks environment for execution and further development.

<img width="1182" alt="clone" src="https://github.com/nogibjj/Individual_Project3_Kelly_Tong/assets/142815940/0117bb7e-c6bb-4485-9a52-1e5805a6bf99">


**6. Job Automation:**
    Create and configure a Databricks job. This job will automate the execution of your data pipeline, streamlining the process and ensuring regular, reliable operation.

## Visualizations

![visual](https://github.com/nogibjj/Individual_Project3_Kelly_Tong/assets/142815940/cef9a6a0-05a1-44c6-8fbf-790954483f22)

## Data Source, Data Sink (Delta Lake), and ETL Pipeline

`Extraction` : Data Source (Individual_Project3_Kelly_Tong/mylib/extract.py) 

`Transform_load`: Data Sink (Delta Lake) (Individual_Project3_Kelly_Tong/mylib/transform_load.py) 

`Query_viz`: perform query and generate visualization task (Individual_Project3_Kelly_Tong/mylib/query_viz.py) 

Job pipeline in Databricks Workflows: 

<img width="765" alt="Individual3 Job Run" src="https://github.com/nogibjj/Individual_Project3_Kelly_Tong/assets/142815940/4375882b-a94e-4e1c-ba57-808f4087f45e">

## Data Source Storing in DBFS

DBFS: 

<img width="1159" alt="DBFS" src="https://github.com/nogibjj/Individual_Project3_Kelly_Tong/assets/142815940/348dc611-d298-4361-a73b-ebf5d1ecae63">

Catalog: 

<img width="1202" alt="catalog data source" src="https://github.com/nogibjj/Individual_Project3_Kelly_Tong/assets/142815940/a138d5db-3ac3-45cb-aab1-730e820b522e">

## Conclusion and Recommendation

The visualization (in visualizations section above) demonstrates that Biology is the most popular discipline with the higest total population (men and women in total) among all selected major. This is, however, different from data included in all_ages.csv. Further research into all_ages and grad_students data have suggested other more popular discipline/major for men and women. This could be caused by the limited majors included in this dataset. Potential recommendation on expanding the sample size and range could benefit the data accuracy and provide more careful and meaningful conclusion. This could also be due to the fact that women_stem.csv is a subset of another dataset, meaning that not the complete view is being provided here. A comparison between women_stem dataset with the original full pictured dataset could be an improvement and extension of the currently approached discovery. 

## Building Process
