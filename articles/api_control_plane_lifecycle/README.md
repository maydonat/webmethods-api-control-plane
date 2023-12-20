## Assessment Questionnaire: Is API Control Plane Suitable for Your Needs?

This section serves as a comprehensive guide for understanding the entire provisioning life cycle and onboarding process for both self-hosted and cloud customers.

1. What is webMethods API Control Plane?

   API Control Plane is a centralized control and monitoring system that oversees and manages multiple runtimes such as API Gateway, Developer Portal, Microgateway, and so on deployed across multiple regions including        cloud and on-premises environments. With API Control Plane, you can achieve comprehensive real-time monitoring, leveraging advanced analytics, and customizable dashboards to gain valuable insights from your data to make data-driven decisions and drive improvements in your organization.

2. What are the deployment variants of API Control Plane?

   - **Cloud**
      - *SAAS Cloud*. Software AG hosts and manages API Control Plane on a cloud-based Software as a Service (SaaS) infrastructure. This fully managed deployment is the recommended choice for ease of management and scalability.
      - *Private Cloud*. If you prefer to deploy API Control Plane in your private cloud environment, you have the flexibility to choose between running the application in docker containers or kubernetes.
   - **On-premises**. You can deploy API Control Plane using docker or helm.

3. Where is API Control Plane hosted?<br>

   Software AG provisions API Control Plane on the Software AG Cloud platform exclusively in the *Azure West Europe* region (Netherlands).

4. How can a customer provision a new API Control Plane tenant?<br>

   webMethods.io API Control Plane is available only for enterprise customers. webMethods.io API Control Plane tenants are provisioned to enterprise customers upon request. Contact Software AG support if you wish to       
   subscribe to API Control Plane.   

6. What Gateways are supported?<br>
   API Control Plane currently supports connectivity with API Gateway version, 10.15 Fix 10 (10.15.0.10) and above, provisioned by Software AG Cloud. 

   - **API Control Plane Cloud** -  Supports connectivity with API Gateway deployed in SAG Cloud and On-premises.
  
   - **API Control Plane On-premises** - Supports connectivity with API Gateway deployed in On-premises.
  
7. What are the Provisioning steps that Cloudops follows when a customer requests for an API Control Plane tenant?<br>

   


8. Is SAG Cloud responsible for connecting your Gateways with API Control Plane?
    


9. Can the domain name of API Control Plane tenant be customized?


10. Certificate management?



12. What are the deployment models of API Control Plane?<br>

    Two common API Control Plane deployment models are:

    - Single node deployment
    - You can set up High availability solution for protection against single point of failure within a single data center or HADR (High Availability and Disaster Recovery) solution for protection from the failure of an         entire data center.

13. Which license is necessary for deploying the on-prem version of API Control Plane?

14. How to deploy the on-prem version of API Control Plane?<br>

    API Control Plane can be deployed using:

    - Docker: For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-deploy_standalone_apicp_docker.html%23
   
    - Helm: For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-deploy_standalone_apicp_docker.html%23
   
15. What are the hardware and product configuration guidelines that are required to deploy API Control Plane to run at an optimal scale?<br>

    See https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fre-resourcing_guidelines.html%23 for details.

16. Where are the logs collected?<br>

    The logs are collected at the location /logs/.

17. What is the process for log rotation in API Control Plane?<br>

    The rolling appender configuration creates logs based on time (daily) and file size (10MB). When a log file size reaches 10MB, a new log file is created, and the older log file is archived. Old log files are archived     in the directory LOGS/archived/microservice_name with a naming pattern that includes the date in the format yyyy-MM-dd. A maximum of 100 archived log files are retained. Once this limit is reached, older log files        are automatically purged to keep the log directory manageable.

    For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-configuring_log_levels.html%23

18. How can a customer handle index management in API Control Plane?<br>

    ILM (Index Lifecycle Management) policy must be defined to manage the Elasticsearch data indices efficiently ensuring optimal data storage and retrieval.

19. Name the list of indices.

    |Type of data|Indice name|
    |-----|-----|
    |**Assets**|tenant_name_assets |
    |**UMC**|api_tenant_name_umc <br> api_master_umc |
    |**Metrics**|.ds-cp_monitoring_data_tenant_name_runtime_metrics <br> .ds-cp_monitoring_job_meta_data_tenant_name_metrics_payload <br> .ds-cp_monitoring_job_meta_data_tenant_name |
    |**Heartbeats**|.ds-cp_monitoring_data_tenant_name_runtime_heartbeats  |
    |**Heartbeats**|.ds-cp_data_tenant_name_audit_events  |


20. What are the index rollover stages in ILM implementation?<br>

    |Tier name|Description|
    |-----|-----|
    |**Hot Tier (0-10 Days)**|This tier typically includes data that is frequently accessed and needs to be readily available for immediate use. <br> Data longer than **10** days are rolled over and moved to *Warm* tier.     |
    |**Warm Tier (10-20 Days)**|This tier usually contains data that is accessed less frequently than hot tier but still requires relatively quick access. <br> Data longer than **20** days are rolled over and moved to 
    *Cold* tier. |
    |**Cold Tier (20-30 Days)**|This tier includes data that is rarely accessed but is retained for compliance, backup, or archival purposes. <br> Data at this tier is intended for read-only purposes.|
    |**Delete Phase (>30 Days)**| This phase refers to data that has exceeded a predefined retention period and is scheduled for deletion. <br> Data longer than 30 days get deleted automatically.|

    For the ILM policy to work as defined in a cluster setup, the cluster health status must be **green**.

    **Cloud**: Logs older than **30** days are purged in Cloud and cannot be retrieved to ensure proper housekeeping.

    For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-data_house_keeping.html%23

21. 


    

    
    


    


