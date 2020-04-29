---

copyright:
  years: 2018, 2020
lastupdated: "2020-03-25"

keywords: LogDNA, IBM Cloud, Log Analysis, logging, customer responsibilities, IBM responsibilities, terms and conditions

subcollection: LogDNA

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}
{:download: .download}
{:preview: .preview}

# Understanding your responsibilities when using {{site.data.keyword.la_full_notm}}
{: #shared-responsibilities}

Learn about the management responsibilities and terms and conditions that you have when you use {{site.data.keyword.la_full}}. For a high-level view of the service types in {{site.data.keyword.cloud_notm}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for {{site.data.keyword.cloud_notm}} offerings](/docs/overview?topic=overview-shared-responsibilities).
{:shortdesc}

Review the following sections for the specific responsibilities for you and for {{site.data.keyword.IBM_notm}} when you use {{site.data.keyword.la_full_notm}}. For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).

  
## Incident and operations management
{: #incident-and-ops}

You and {{site.data.keyword.IBM_notm}} share responsibilities for the set up and maintenance of your {{site.data.keyword.la_full_notm}} service instance and infrastructure workloads. You are responsible for incident and operations management of your data.
{: note}

| Task              | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|-------------------|-------------------------------------------------|-----------------------|
| `Monitor incidents`  | Provide notifications for planned maintenance, security bulletins, or unplanned outages. | Set preferences to [receive emails about platform notifications](/docs/overview?topic=overview-ui#email-prefsl). </br>Monitor the [IBM Cloud status page](https://{DomainName}/status?selected=announcement) for general announcements. |
| `Maintain {{site.data.keyword.cloud_notm}} high availability SLA`  | Provide Cloud Service across availability zones in a Multi-Zone Region (MZR). </br> Provide Cloud Service across hosts in a Single-Zone Region (SZR). </br>Provides replication, fail-over features, and infrastructure maintenance and updates. | Use the [list of available regions](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-regions) to plan for and create new instances of the service. |
| `Monitor platform logs`  | [Participating Cloud services](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-cloud_services) publish relevant log data to their subscribing clients. {{site.data.keyword.la_full_notm}} provides clients with the ability to receive the logs once the client configures their instance. | [Create an {{site.data.keyword.la_full_notm}} instance](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-provision) in each region where Cloud service subscriptions publish logs. </br>[Configure 1 instance in each of those regions to received the published logs](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-config_svc_logs). |
| `Monitor logs collected by LogDNA agents`   | Provide images and instructions for how to install LogDNA agents in environments that you want to monitor, such as Kubernetes, Linux, Openshift. | Install and configure LogDNA agents. </br>Monitor that the agents are running in your environment. |
| `Archive logs`  | Provide the ablity to archive to a client configured Cloud Object Storage (COS) location and archive data hourly or daily. | [Configure Cloud Object Storage per your requirements.](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-archiving#archiving_step3) </br>[Enable archiving of the logging instance.](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-archiving) |
{: caption="Table 1. Responsibilities for incident and operations" caption-side="top"}


		


## Change management
{: #change-management}

You and {{site.data.keyword.IBM_notm}} share responsibilities for keeping {{site.data.keyword.la_full_notm}} service components at the latest version. You are responsible for change management of your LogDNA agents, dashboards, screens, views, and alert definitions.
{: note}

| Task                                                    | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|---------------------------------------------------------|-----------------------|--------|
| `Update the {{site.data.keyword.la_full_notm}} service` | Provide major, minor, and patch version updates for {{site.data.keyword.la_full_notm}} interfaces. </br>Document changes in the [LogDNA release notes](https://logdna.zendesk.com/hc/en-us/categories/360001626492-Release-Notes) | Ensure that any LogDNA agents that you have deployed are kept current. |
| `Track versions of custom views, dashboards, screens, parsing templates, and alerts`    | `N/A` | Use your own change management process to control versions of logging resources such as views, dashboards, screens, parsing templates, and alerts`. </br>To learn how to export metadata, see [Export the configuration of resources in a LogDNA instance](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-reuse_resource_definitions#export_config).| 
{: caption="Table 2. Responsibilities for change management" caption-side="top"}


## Identity and access management
{: #iam-responsibilities}

{{site.data.keyword.IBM_notm}} is responsible for the security and compliance of {{site.data.keyword.la_full_notm}}. You are responsible for defining the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) policies to control which users within your account have access to the logging data.
{: note}

| Task                           | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|--------------------------------|-------------------------------------------------|-----------------------|
| `Manage permissions`           | Provide the ability to restrict access to resouces. | Depending on your needs, restrict access to resources by using Cloud IAM access policies. </br>[Learn more about controlling access through IAM](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-iam). | 
{: caption="Table 3. Responsibilities for identity and access management" caption-side="top"}





## Security and regulation compliance
{: #security-compliance}

{{site.data.keyword.IBM_notm}} is responsible for the security and compliance of {{site.data.keyword.la_full_notm}}. You are responsible for ensuring that logs, that contain regulated data, are not provided to the {{site.data.keyword.la_full_notm}} service.
{: note}

| Task                                       | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|--------------------------------------------|-------------------------------------------------|-----------------------|
| `Encrypt data`  | Operate the Cloud Service encrypting data in motion and at rest per compliance specifications. | Ensure encryption of archived data by configuring a COS bucket that has full control over the data encryption keys that are used. [{{site.data.keyword.cos_full}} provides several options to encrypt your data.](/docs/cloud-object-storage?topic=cloud-object-storage-encryption). |
| `Meet security and compliance objectives`  | Maintain controls that are commensurate to various industry compliance standards such as SOC2, PCI, HIPAA and Privacy Shield. | Set up and maintain security and regulation compliance for your apps and data.  This includes: </br>[Defining the account management strategy](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-adoption#adoption_account) </br>[Configuring the accounts settings for compliance](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-adoption#adoption_acc_settings) </br>Define IAM Strategy </br>[Define the notification strategy](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-adoption#adoption_alerts) |
{: caption="Table 4. Responsibilities for security and regulation compliance" caption-side="top"}


## Disaster recovery
{: #disaster-recovery}

{{site.data.keyword.IBM_notm}} is responsible for the recovery of {{site.data.keyword.la_full_notm}} components in case of disaster. You are responsible for the recovery of the LogDNA agents running in your environment should they be impacted by a disaster, and the resources to manage metadata like views, dashboards, screens, parsing templates, and alerts.
{: note}

| Task                                                            | {{site.data.keyword.IBM_notm}} Responsibilities | Your Responsibilities |
|-----------------------------------------------------------------|-------------------------------------------------|-----------------------|
| `Restore the service` `[*]`      |Automatically recover and restart service components after any disaster event.  | `N/A` |
| `Backup the {{site.data.keyword.la_full_notm}} service`        | Daily backup of the {{site.data.keyword.la_full_notm}} infrastructure and components. | `N/A` |
| `Backup LogDNA agents`                                          | `N/A`  | Backup each LogDNA agent yaml file that is deployed in your organization. |
| `Recovery of LogDNA agents`                                     | `N/A` | [Reinstall](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-logdna_agent#logdna_agent_configure) the LogDNA agent in the event of any disaster event that impacts the agent runtime. |
| `Backup the metadata of a LogDNA instance`                          | `N/A` | [Backup the metadata such as views, dashboards, screens, parsing templates, and alerts for each LogDNA instance.](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-reuse_resource_definitions#export_config) |
| `Restore the metadata of a LogDNA instance`                         | `N/A` | [Restore the metadata such as views, dashboards, screens, parsing templates, and alerts for each LogDNA instance.](/docs/Log-Analysis-with-LogDNA?topic=LogDNA-reuse_resource_definitions#import_config) |
{: caption="Table 5. Responsibilities for disaster recovery" caption-side="top"}


`[*]` Recovered and restarted service components will not have customer data reloaded.
{: note}
