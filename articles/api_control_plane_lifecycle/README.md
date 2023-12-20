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
  
7. What are the Provisioning steps that Cloudops follows when a customer requests for an API Control Plane tenant?


8. Is SAG Cloud responsible for connecting your Gateways with API Control Plane?


9. Can the domain name of API Control Plane tenant be customized?


10. Certificate management


11. What licenses are required to deploy API Control Plane in On-premises?


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

16. In which location are the logs collected?<br>

    The logs are located at the location /logs/.

18. What is the process for log rotation in API Control Plane?<br>

    The rolling appender configuration creates logs based on time (daily) and file size (10MB). When a log file size reaches 10MB, a new log file is created, and the older log file is archived. Old log files are archived      in the directory LOGS/archived/microservice_name with a naming pattern that includes the date in the format yyyy-MM-dd. A maximum of 100 archived log files are retained. Once this limit is reached, older log files         are automatically purged to keep the log directory manageable.

    For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-configuring_log_levels.html%23

19. 
    

    
    


    


