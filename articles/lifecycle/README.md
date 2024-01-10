## All about API Control Plane

This section serves as a comprehensive guide for understanding the life cycle of API Control Plane.

1. What is webMethods API Control Plane?

   API Control Plane is a centralized control and monitoring system that oversees and manages multiple runtimes such as API Gateway, Developer Portal, Microgateway, and so on deployed across multiple regions 
   including cloud and on-premises environments. With API Control Plane, you can achieve comprehensive real-time monitoring, leveraging advanced analytics, and customizable dashboards to gain valuable insights 
   from your data to make data-driven decisions and improvements in your organization.

2. What are the deployment variants of API Control Plane?

   - **Cloud**
      - *SAAS Cloud*. Software AG hosts and manages API Control Plane on a cloud-based Software as a Service (SaaS) infrastructure. Opting for this fully managed deployment is the recommended choice for ease of 
         management and scalability.
      - *Private Cloud*. If you prefer to deploy API Control Plane in private cloud environment, you have the flexibility to choose between running the application in docker containers or kubernetes.
   - **On-premises**. You can deploy API Control Plane using docker or helm.

3. Where is API Control Plane Cloud hosted?<br>

   Software AG provisions API Control Plane on the Software AG Cloud platform exclusively in the *Azure West Europe* region (Netherlands).

4. How can you request for a new API Control Plane tenant?<br>

   webMethods.io API Control Plane is available only for enterprise customers. webMethods.io API Control Plane tenants are provisioned to enterprise customers upon request. Contact Software AG support if you wish 
   to subscribe to API Control Plane.

5. What is the process for upgrading an API Control Plane tenant to a new version?<br>

   API Control Plane tenants are automatically upgraded to the latest version by Software AG Cloud Ops.

6. What is the downtime for the upgrade process?

   No downtime.

7. How are the upgrade notifications communicated to the customers?<br>

   Upgrade notifications are sent through the [Status page](https://status.webmethods.io/) and e-mails. The status page has information on major releases, hotfixes, and patch releases including the latest 
   statistics on cloud environments availability, incident history, and planned maintenance events.
   
8. How are Rollback procedures handled?

    In terms of failure during the upgrade process, Software AG Cloud Ops handles the rollback procedure.
   
9. What Gateways are supported?<br>

   API Control Plane currently supports connectivity with Software AG - API Gateway (version 10.15 Fix 10 and above).  

11. Can the domain name of API Control Plane tenant be customized?

    Yes. Create a support ticket for a custom domain.

12. How are the certificates managed?

    Software AG Cloud Ops handles the certificate management. Create a support ticket if you have a requirement. 

13. How are the users managed?<br>

    **User Management in Software AG Cloud**

    You can manage user’s information from the Administration page in Software AG Cloud.

    **Users**: There are two user personas, *Cloud-Tenant-Administrator* and *APIControlPlane-User* depending on the roles assigned to the users. 
    Based on the user groups assigned, user can access API Control Plane.

    >**Note**: Only the Cloud-Tenant-Administrators can create, modify, and delete users.

    **User groups in API Control Plane**

    The following predefined user groups can access API Control Plane:

    *	API Control Plane administrators
    *	API platform providers
    *	API product managers
    
    For details on the privileges based on the user groups, see https://docs.webmethods.io/apicontrolplane/administration/chapter3wco#co-user_management

14. What is the deployment model of API Control Plane?<br>

    API Control Plane can be deployed using High availability solution for protection against single point of failure within a single data center or HADR (High Availability and Disaster Recovery) solution for 
    protection from the failure of an entire data center.

15. How to deploy the on-prem version of API Control Plane?<br>

    API Control Plane can be deployed using:

    - Docker: For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-deploy_standalone_apicp_docker.html%23
   
    - Helm: For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-deploy_standalone_apicp_docker.html%23
   
16. How to connect API Gateway with API Control Plane?<br>

    To connect API Control Plane using API Gateway UI, see *Configuring API Control Plane* section in *API Gateway Administration* guide.

    To connect API Control Plane using properties or YAML file, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-connecting-apigw.html%23
   
18. What are the hardware and product configuration guidelines that are required to deploy API Control Plane to run at an optimal scale?<br>

    For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fre-resourcing_guidelines.html%23

19. How to manage data backups/snapshot to ensure data resiliency and disaster recovery?<br>

    For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-snapshot_management.html%23

20. Does API Control Plane provide REST endpoints to monitor the health and resource utilization of the microservices and Elastic search?<br>

    Yes. For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-monitor_apicp.html%23

21. List the Prometheus metrics to analyze API Control Plane health.<br>

    For details, see https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fco-collect_microservices_metrics.html%23

22. Is Open telemetry supported for tracing?<br>

    Yes. To deploy API Control Plane enabling Open Telemetry using Jaeger UI with Docker, perform *step 5* mentioned in
    https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fta-deploy_standalone_apicp_docker.html%23

23. Can Gainsight be integrated with API Control Plane?

    Yes. You can integrate Gainsight with API Control Plane Cloud for user engagements such as bots, articles, feature introduction, etc.. For details, see [https://github.com/Kirthi08/webmethods-api-control- 
    plane/tree/main/deployment/docker#additional-deployment-flavors](https://github.com/SoftwareAG/webmethods-api-control-plane/tree/main/deployment/docker#additional-deployment-flavors)


## FAQ's

1. How do I report an incident?<br>

   You can report an incident through our Service Portal, [JSM](https://getsupport.softwareag.com/)


## References

* Official On-prem documentation link: https://documentation.softwareag.com/wco/11.0.0/en/webhelp/wco-webhelp/#page/wco-webhelp%2Fto-landing_page.html%23
* Official Cloud documentation link: https://docs.webmethods.io/apicontrolplane/welcome/home/#gsc.tab=0

    


    

    
    


    


