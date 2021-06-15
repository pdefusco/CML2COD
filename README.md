# CML COD Integration Quickstart

This project demonstrates how to use a Cloudera Operational Database instance in conjunction with Cloudera Machine Learning

## Project Overview

There are two sections:

1) Setup & Prerequisites
2) Demonstration

### Setup & Requirements

In order to make this work, we assume you have set up IDBroker Mappings and Ranger permissions in CDP. For documentation on how to do that please use the follwoing links:

Link 1
Link 2

##### Environment Variable Setup

In this step we will create three environment variables in the CML Project.

1) COD_ENDPOINT
2) WORKLOAD_USER
3) WORKLOAD_PASSWORD

To find the OpDB endpoint, navigate to the CDP Home Page and open the COD service. 

Select the database instance you will connect to, and open the "Phoenix (Thin)" tab.

Copy the url value from the JDBC URL string. You only need to copy starting from "https" and up to and including "avatica".

For example: "https://cod-xxxxx-gatewayxxxx.demo-aws.xxxxx.cloudera.site/cod-xxxxx/cdp-proxy-api/avatica"

![alt_text](https://github.com/pdefusco/myimages_repo/blob/main/COD_screenshot.png)

Next, open your CML Project from the CML workspace main page.

![alt_text](https://github.com/pdefusco/myimages_repo/blob/main/cml_project.png)

Navigate to "Project Settings" and open the "Advanced" tab.

Enter the three environment variables in the "Name" and "Value" fields respectively as shown below

![alt_text](https://github.com/pdefusco/myimages_repo/blob/main/environ_vars.png)


##### Demonstration

Start a CML Session with the following settings:

- Name: enter a name of your preference
- Editor: JupyterLab
- Kernel: Python 3 (any version of Python 3 will work)
- Edition: Standard
- Resource Profile: 1 vCPU / 2GiB Memory

The notebook contains instructions. If you are new to Jupyter Notebooks, you can execute each cell by pressing "Shift Command Enter" at the same time on your keyboard.
