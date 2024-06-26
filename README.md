## Introduction: 
In today’s IT organization, it’s not a question of whether or not public cloud resources are used for production applications, but which application should be deployed there. For modern digital businesses, capacity and cost management are essential to ensure adequate resources and budget, whether on-premises or in the cloud, to support new, existing, and growing business services. Nowadays most of the organizations from small scale to large scale are switching 80% of their operations to the cloud. According to Gartner, approximately 28 percent of server capacity currently goes unused, as well as 40 percent of storage. 
Capacity management informs forecasting and planning by helping you determine the capacity levels that you’ll notice across your environment, including computing configurations, storage, database, and network bandwidth, as well as the most cost-effective way to provision them. 

## Recommenders: 
A recommender is a service on Google Cloud that provides usage recommendations for Google Cloud resources. Recommenders are specific to a single Google Cloud product and resource type. A single product can have multiple recommenders, where each provides a different type of recommendation for a different resource.
In Recommender we can divide in following categories:
1.	Cost Recommenders.
2.	Security Recommenders.
3.	Performance Recommenders.
4.	Manageability Recommenders.
5.	Sustainability Recommenders.

## Cost Recommenders:
1.	__Idle persistent disk recommender__: Compute Engine provides recommendations to help you identify resources like persistent disks (PDs) that aren't used. You can use idle persistent disk recommender to help minimize waste of resources and reduce your compute bill. For PDs that are not actively used, you can create a backup snapshot then delete the resource. By taking backup and deleting the PD it Reduce the maintenance cost of that disk by 35% to 92% and Save 100% of the cost of that disk.
2.	__Idle custom image recommender__: Compute Engine provides recommendations to help you identify resources like custom disk images that aren't used. You can use idle custom image recommender: to help minimize waste of resources and reduce your compute bill. For images you can delete them if you don't need them and Save 100% of the cost of that image. 
3.	__Idle IP address recommender__: Compute Engine provides recommendations to help you identify resources like IP addresses that aren't used. You can use idle IP address recommender to help minimize waste of resources and reduce your compute bill. For PDs that are not actively used, you can create a backup snapshot then delete the resource. For unused PDs, images, and IP addresses, you can delete them if you don't need them. Save 100% of the cost of that IP address.
4.	__Idle VM recommendations__: Compute Engine provides idle VM recommendations to help you identify virtual machine (VM) instances that have not been used. These recommendations are generated automatically based on system metrics gathered by the Cloud Monitoring service over the previous 14 days. You can use idle VM recommendations to find and stop idle VM instances to reduce waste of resources and reduce your compute bill.
5.	__BigQuery Slot recommender__: The BigQuery slot recommender creates recommendations for customers using on-demand billing. These recommendations help you to understand your BigQuery capacity needs, as well as the cost and performance tradeoffs of purchasing different amounts of slot capacity. Slot recommendations might include a range of options, depending on whether you want to optimize for cost or performance. For example, the recommender might recommend purchasing 5000 monthly slots at p99 or 2500 monthly slots at p90. The second option would cost less, but is based on the p90 usage, so it might result in lower performance some of the time. At p100, the recommendation would cover all queries in the historical data with no impact on performance.
6.	__Cloud SQL idle instance recommender__: The Cloud SQL idle instance recommender helps you detect instances that might be idle and provides you insights and recommendations to help you reduce costs. 
7.	__Cloud SQL overprovisioned instance recommender__: The Cloud SQL overprovisioned instance recommender helps you detect instances that are unnecessarily large for a given workload. It then provides recommendations on how to resize such instances and reduce cost. If the peak utilization of either or both the CPU and the memory within the observation period is low, the instance is estimated to be overprovisioned. Recommendations are generated every 24 hours for rightsizing such instances when the estimated monthly cost savings are greater than or equal to $10.The recommender uses conservative thresholds to ensure that it flags only instances that are significantly overprovisioned, which is usually a good indicator of waste. The recommender suggests a machine type that has at least 4 vCPUs and 26 GB.
8.	__Committed use discount recommender__: The committed use discount (CUD) recommender helps you optimize the resource costs of the projects in your Cloud Billing account. Its recommendations are generated automatically based on historical usage metrics gathered by Cloud Billing. You can use these recommendations to purchase additional commitments and further optimize your Google Cloud costs. 
      - __Stable usage recommendations__: Stable usage recommendations take into account the minimum stable spending or usage for your account over the last 30 days. If your projects show a trend of uncommitted usage during that period, the recommender classifies this as an opportunity to purchase committed use discounts to reduce your costs.
      - __Optimal recommendations__: Optimal recommendations take into account overall historical usage, up to the most recent 30 days, including times when you exceeded the minimal stable spending or usage. These recommendations help you maximize savings associated with projects that experience periodic increases that aren't included in the stable usage calculations. When your spending or usage fluctuates over time, purchasing commitments at minimal stable usage might not give you the most cost savings. Optimal recommendations account for fluctuations in your usage and provide further cost savings.
## Security Recommenders:
1.	__Account security recommender__: The account security recommender prompts Google Cloud project owners to protect their account with their phone's built-in security key. If a project owner has an eligible device associated with their account and isn't using a third party Identity provider for single sign-on, a notification shows in Google Cloud console's Notifications notifications menu. The project owner can then choose to enable their phone as a security key for their account, or dismiss the notification.
2.	__IAM recommender__: Role recommendations are one of the types of recommendations that Recommender generates. Each role recommendation suggests that you remove or replace a role that gives your principals excess permissions. At scale, these recommendations help you enforce the principle of least privilege by ensuring that principals have only the permissions that they actually need. Recommender identifies excess permissions using policy insights. Policy insights are ML-based findings about a principal's permission usage. Some recommendations are also associated with lateral movement insights. These insights identify roles that allow service accounts in one project to impersonate service accounts in another project.
3.	__Google Maps Platform project management recommender__: The project management recommender helps you improve the health of your Google Maps Platform project. For instance, if your project doesn't have secure API keys, the recommender can help restrict these keys in order to secure your account.
4. __Cloud Run Service Identity recommender__: This recommender provides the following recommendations:
    * Service account might have more permissions than required.
    * Environment variable might contain a password.
    * Environment variable might contain an API key.
    * Environment variable might contain Google Application Credentials.

## Performance Recommenders.
1.	__Cloud SQL out-of-disk recommender__: The Cloud SQL out-of- disk recommender proactively generates recommendations that help you reduce the risk of downtime that might be caused by your instances running out of disk space. You can apply these recommendations when a Cloud SQL instance is trending toward a storage limit. 
2.	__Managed instance group machine type recommender__: Compute Engine provides machine type recommendations for managed instance groups (MIGs) to help you improve workload performance and cost efficiency. Use these recommendations to determine whether you should resize the machine type of your instances to add or remove vCPU and memory resources.
3.	__VM machine type recommender__: Compute Engine provides machine type recommendations to help you optimize the resource utilization of your virtual machine (VM) instances. These recommendations are generated automatically based on system metrics gathered by the Cloud Monitoring service over the previous 8 days. Use these recommendations to resize your instance's machine type to more efficiently use the instance's resources. This feature is also known as rightsizing recommendations.

## Manageability Recommenders.
1.	__Error Reporting notification recommender__: The Error Reporting recommender looks for recent crashes in your Google Cloud project and provides recommendations if you have not configured Error Reporting notifications. When you have notifications configured, no recommendations are made.
2.	__Product suggestion recommender__: The product suggestion recommender helps you to optimize your Cloud usage by providing you with product suggestions. This can help you improve performance and security, and manage your resources better. Based on best practices, it analyzes your current product usage within each project and determines any additional products that might optimize your usage. If the recommender identifies an opportunity to leverage a product within a project, a recommendation is generated for that project in the Recommendation Hub. All users who have the appropriate permissions can view the recommendations when logged in to the hub. Every product suggestion includes information about the recommendation, details on the product, and links to help you get started with the product.
3. __Container diagnosis recommender (PREVIEW)__:  When GKE detects that a cluster is using a Kubernetes feature or API that is deprecated and will be removed in an upcoming minor version, the following happens:
    * Automatic upgrade to the upcoming minor version is paused. To learn more about how this works, see What happens when GKE pauses automatic upgrades.
    * An insight and recommendation are generated so that you can assess and mitigate your cluster's exposure to the deprecation.
Deprecation insights and recommendations are available from Recommender, a service that provides insights and recommendations for using resources on Google Cloud. For the deprecations topic with Recommender:
•	An insight explains that your cluster uses a feature or API that is deprecated and will be removed in an upcoming minor version.
•	A recommendation provides guidance on what to do to mitigate your cluster's exposure to the deprecation.
## Sustainability Recommenders.
1.	__Unattended project recommender__: The unattended project recommender analyses usage activity on projects in your organization and provides recommendations that help you discover, reclaim or remove unattended projects. Unattended project recommender analyzes usage activity across all projects in your organization and provides you with the following features to help you discover, reclaim, and shut down unattended projects: 
    * Usage insights for every project (networking, API, project owner, service activity, and more).
    * Recommendations to turn down projects having low usage activity.
    * Recommendations to assign a new owner to projects that have high usage activity but no active owner.
1. __Unattended project recommender__: The unattended project recommender analyses usage activity on projects in your organization and provides recommendations that help you discover, reclaim or remove unattended projects. Unattended project recommender analyzes usage activity across all projects in your organization and provides you with the following features to help you discover, reclaim, and shut down unattended projects: 
    * Usage insights for every project (networking, API, project owner, service activity, and more).
    * Usage insights for every project (networking, API, project owner, service activity, and more).
    * Recommendations to turn down projects having low usage activity.
    * Recommendations to assign a new owner to projects that have high usage activity but no active owner.

Shutting down or reclaiming unattended projects can provide the following impact and benefits to your organization:
  * Reduction in security risks (SECURITY).
  * Reduction in unnecessary spending (COST).
  * Reduction in carbon footprint associated with your workloads (SUSTAINABILITY).




