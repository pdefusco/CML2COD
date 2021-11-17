# CML2COD

This project demonstrates how to use a Cloudera Operational Database instance in conjunction with Cloudera Machine Learning


## Project Overview

There are two sections:

1) Setup & Prerequisites
2) Demonstration


### Setup & Prerequisites

In order to make this work, we assume you have set up your CDP environment, IDBroker Mappings and Ranger permissions in CDP. 

For instructions on how to do that please use the follwoing links:

- [Getting Started with CDP](https://docs.cloudera.com/cdp/latest/index.html)

- [ID Broker Mappings](https://docs.cloudera.com/runtime/7.2.0/cdp-security-overview/topics/security_how_identity_federation_works_in_cdp.html)

- [Ranger Permissions in CDP](https://docs.cloudera.com/runtime/7.2.2/security-ranger-authorization/topics/security-ranger-provide-authorization-cdp.html)


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

Run the "COD_Demo" notebook. The notebook does not require any changes to the code and contains instructions. 
If you are new to Jupyter Notebooks, you can execute each cell by pressing "Shift Command Enter" at the same time on your keyboard.
