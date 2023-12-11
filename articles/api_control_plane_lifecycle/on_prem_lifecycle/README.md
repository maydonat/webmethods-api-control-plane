## API Control Plane On-premises Life cycle

## Official On-prem documentation link:  
https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/

***

Table of contents

1. [Deloyment models](#deployment-models) 
2. [Licensing](#licensing)
3. [Hardware and Product configurations](#hardware-and-product-configurations)
4. [Deployment](#deployment)
5. [Log Management](#log-management)
6. [Data Housekeeping](#data-housekeeping)
7. [Monitoring](#monitoring)
8. [Functionalities](#functionalities)
9. [User Management](#user-management)

***


## Deployment models

Two common API Control Plane deployment models are:

*	Single node deployment
*	You can set up High availability solution for protection against single point of failure within a single data center or HADR (High Availability and Disaster Recovery) solution for protection from the failure of an entire data center.

For details, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-deployment.html%23


## Licensing 



## Hardware and Product configurations

The hardware and product configuration guidelines are required to setup API Control Plane to run at an optimal scale. For details about the sizing guidelines, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fre-resourcing_guidelines.html%23


## Deployment

*	For details about how to install and run API Control Plane using Docker, follow the instructions in https://github.com/SoftwareAG/webmethods-api-control-plane/tree/main/deployment/docker

*	For details about how to install and run API Control Plane on Kubernetes using Helm, follow the instructions in https://github.com/SoftwareAG/webmethods-api-control-plane/tree/main/deployment/helm

*	For details about how to connect API Gateway with API Control Plane, follow the instructions in https://github.com/SoftwareAG/webmethods-api-control-plane/blob/main/deployment/agent/webmethods-api-gateway/README.md


## Log Management

Log management is essential for maintaining and monitoring the health and performance of API Control Plane.  For details, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-configuring_log_levels.html%23


## Data Housekeeping

Data housekeeping refers to systematically managing and maintaining data in API Control Plane to ensure its accuracy, reliability, and usability throughout its lifecycle and to prevent any performance or capacity problems.

API Control Plane records assets, metrics, and log data. As a result, the amount of data maintained by API Control Plane grows considerably and the older or obsolete data must be removed or purged.

For details, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-data_mgmt.html%23

## Monitoring

Monitoring API Control Plane is essential to:

*	Identify performance issues
*	Track usage and traffic
*	Early issue detection
*	Improve service availability

API Control Plane provides REST endpoints to monitor the health and resource utilization of the microservices. For details, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-monitor_apicp.html%23


## Functionalities

For details about the capabilities offered by API Control Plane, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/


## User Management

The following predefined user groups can access API Control Plane:

*	API Control Plane administrators
*	API platform providers
*	API product managers

Privileges based on the user groups:<br>
![image](/attachments/users_privileges.png)
![image](/attachments/data_plane_privileges.png)
![image](/attachments/runtime_privileges.png)
![image](/attachments/apis_privileges.png)

For details, see https://documentation.softwareag.com/wco/10.16.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-user_management.html%23
