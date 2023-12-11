## API Control Plane On-premises Life cycle

## Official Cloud documentation link: https://docs.webmethods.io/apicontrolplane/10.16.0/welcome/home/#gsc.tab=0

***

Table of contents

1. [Where is API Control Plane Cloud hosted?](#where-is-api-control-plane-cloud-hosted) 
2. [How to subscribe for an API Control Plane tenant?](#how-to-subscribe-for-an-api-control-plane-tenant)
3. [Provisioning steps by Cloudops](#provisioning-steps-by-cloudops)
4. [SAG Cloud wiring](#sag-cloud-wiring)
5. [Custom Domain](#custom-domain)
6. [Certificate Management](#certificate-management)
7. [What Gateways can be connected with API Control Plane?](#what-gateways-can-be-connected-with-api-control-plane)
8. [Functionalities](#functionalities)
9. [User Management](#user-management)
10. [API Control Plane decommissioning](#api-control-plane-decommissioning)
11. [Data housekeeping](#data-housekeeping)
12. [Autoscaling](#api-control-plane-autoscaling)
13. [Backup Procedures](#backup-procedures)
14. [Disaster Recovery](#disaster-recovery)
15. [Configurations](#configurations)
16. [Upgrade procedures](#upgrade-procedures)
17. [Monitoring and Alerting](#monitoring-and-alerting)
18. [FAQs](#faqs)
19. [Troubleshooting Tips](#troubleshooting-tips)

***


## Where is API Control Plane Cloud hosted?

Software AG provisions API Control Plane on the Software AG Cloud platform exclusively in the Azure West Europe region (Netherlands). Users registered with Software AG Cloud and having the required user roles assigned can access API Control Plane. See Software AG Cloud regions page for information on the available products and underlying infrastructure,  https://www.softwareag.cloud/site/regions.html

For details about the IP addresses for API Control Plane in the Azure West Europe region, see https://docs.webmethods.io/softwareagcloud/allowed_ips/cloudproducts/#gsc.tab=0


## How to subscribe for an API Control Plane tenant?

webMethods.io API Control Plane is available only for enterprise customers. webMethods.io API Control Plane tenants are provisioned to enterprise customers upon request. Contact [Software AG support](https://www.softwareag.com/en_corporate/contact.html) if you wish to subscribe to API Control Plane.


## Provisioning steps by Cloudops
questionnaire


## SAG Cloud wiring

SAG Cloud is resposible for connecting your Gateways (provisioned by Software AG Cloud) with API Control Plane.


## Custom Domain


## Certificate Management


## What Gateways can be connected with API Control Plane?

API Control Plane currently supports connectivity with Gateways provisioned by Software AG Cloud. Contact [Software AG support](https://www.softwareag.com/en_corporate/contact.html) for connecting your Gateways with API Control Plane tenant.


## Functionalities

For details about the capabilities offered by API Control Plane, see  https://docs.webmethods.io/apicontrolplane/10.16.0/welcome/home/#gsc.tab=0


## User Management

**User Management in Software AG Cloud**

You can manage user’s information from the Administration page in Software AG Cloud.

**Users**: User personas who can access API Control Plane and perform tasks. There are two user personas, *Cloud-Tenant-Administrator* and *APIControlPlane-User* depending on the roles assigned to the users. Based on the user groups assigned, user can access API Control Plane.

>**Note**: Only the Cloud-Tenant-Administrators can create, modify, and delete users.

**User groups in API Control Plane**

The following predefined user groups can access API Control Plane:

*	API Control Plane administrators
*	API platform providers
*	API product managers

Privileges based on the user groups:<br>
![image](/attachments/users_privileges.png)
![image](/attachments/data_plane_privileges.png)
![image](/attachments/runtime_privileges.png)
![image](/attachments/apis_privileges.png)

For details, see https://docs.webmethods.io/apicontrolplane/10.16.0/user_management/chapter7wco#gsc.tab=0


## API Control Plane decommissioning

How can a customer raise a decommissioning request?


### Data retention in Cloud

For security and auditing purposes, the audit events log every action performed by API Control Plane, including system transactions, events, and occurrences of specific events (for example, login attempts).

The audit event log data accumulates over time and takes up storage space. Additionally, as the amount of data grows, it becomes difficult to manage the data effectively, which impacts overall performance. Therefore, the audit event logs older than **30** days are purged in Cloud and cannot be retrieved to ensure proper housekeeping.


### How long do we hold the backup if customer comes back?


### Can we get the same domain and old data back?


### API Control plane licensing in Cloud



## Data housekeeping

Data housekeeping refers to systematically managing and maintaining data in API Control Plane to ensure its accuracy, reliability, and usability throughout its lifecycle and to prevent any performance or capacity problems.

API Control Plane records assets, metrics, and log data. As a result, the amount of data maintained by API Control Plane grows considerably and the older or obsolete data must be removed or purged. Therefore it is essential to manage Elasticsearch data indices efficiently.

### List of indices

|Type of data|Indice name|
|-----|-----|
|**Assets**|tenant_name_assets |
|**UMC**|api_tenant_name_umc <br> api_master_umc |
|**Metrics**|.ds-cp_monitoring_data_tenant_name_runtime_metrics <br> .ds-cp_monitoring_job_meta_data_tenant_name_metrics_payload <br> .ds-cp_monitoring_job_meta_data_tenant_name |
|**Heartbeats**|.ds-cp_monitoring_data_tenant_name_runtime_heartbeats  |
|**Heartbeats**|.ds-cp_data_tenant_name_audit_events  |

### ILM implementation

ILM (Index Lifecycle Management) policy is defined to manage the Elasticsearch data indices efficiently ensuring optimal data storage and retrieval.

**Index rollover stages**: 

|Tier name|Description|
|-----|-----|
|**Hot Tier (0-10 Days)**|This tier typically includes data that is frequently accessed and needs to be readily available for immediate use. <br> Data longer than **10** days are rolled over and moved to *Warm* tier. |
|**Warm Tier (10-20 Days)**|This tier usually contains data that is accessed less frequently than hot tier but still requires relatively quick access. <br> Data longer than **20** days are rolled over and moved to *Cold* tier. |
|**Cold Tier (20-30 Days)**|This tier includes data that is rarely accessed but is retained for compliance, backup, or archival purposes. <br> Data at this tier is intended for read-only purposes.|
|**Delete Phase (>30 Days)**| This phase refers to data that has exceeded a predefined retention period and is scheduled for deletion. <br> Data longer than 30 days get deleted automatically.|

For the ILM policy to work as defined in a cluster set up, the cluster health status must be **green


## API Control Plane Autoscaling

### Number of data planes?


### Number of runtimes?


### Transaction limit?


### Chaos??


### Soak?


## Backup Procedures


## Disaster Recovery 


## Configurations

## Upgrade procedures

API Control Plane tenants are automatically upgraded to the latest version.

### Schedules

### Downtime

### Notifications
Upgrade notifications are sent through the [Status page](https://status.webmethods.io/) and e-mails.


### Rollback procedures



## Monitoring and Alerting

### Prometheus


### Open telemetry

Open telemetry allows you to monitor the performance of API Control Plane through tracing. It enables you to discover, analyse, and debug issues before it adversely impacts the application. It provides insights into the lifecycle of each request reaching API Control Plane.

To deploy API Control Plane enabling Open Telemetry using Jaeger UI with 
Docker, see “Deploy a stand alone API Control Plane using Docker” section in 
Getting Started guide.

### Status page updates

Information on major releases, hotfixes, and patch releases including the latest statistics on cloud environments availability, incident history, and planned maintenance events are available on the [webMethods.io iPaaS Service Status page](https://status.webmethods.io/).


## FAQ's

### How do I add an additional Gateway?


### How do I report an incident?

You can report an incident through our Service Portal, [JSM](https://getsupport.softwareag.com/)


## Troubleshooting Tips


1. How to enable on prem logs?















