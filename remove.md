---

copyright:
  years:  2018, 2021
lastupdated: "2021-03-28"

keywords: IBM, Log Analysis, logging instance, delete

subcollection: log-analysis

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:important: .important}
{:note: .note}
{:external: target="_blank" .external}

# Removing an instance
{: #remove}

You can remove an instance of the {{site.data.keyword.la_full_notm}} service from the {{site.data.keyword.cloud_notm}} UI or through the command line.
{:shortdesc}

When you remove an instance from the {{site.data.keyword.cloud_notm}}, clean up by completing the following tasks:

1. Write down the list of sources that forward metrics to the {{site.data.keyword.la_full_notm}} instance that you want to remove. You must remove the logging agent from each source.
2. Remove permissions that are granted to users to work with the instance. 

    If you manage access by using dedicated access groups to work with a specific instance, you must remove these access groups.

    If you manage access to multiple logging instances by using access groups, you must remove the policies that grant permissions to the instance that you want to remove.
    
    If you grant individual policies to users, you must gather the list of users that have permissions to work with that instance. Then, for each user that you identify, you must remove the policies that relate to the instance that you want to delete.


Then, delete the instance from the {{site.data.keyword.cloud_notm}} Dashboard.


## Removing an instance through the {{site.data.keyword.cloud_notm}} UI
{: #remove_ui}

To remove an instance of {{site.data.keyword.la_full_notm}} by using the {{site.data.keyword.cloud_notm}} UI, complete the following steps:

1. [Log in to your {{site.data.keyword.cloud_notm}} account](https://cloud.ibm.com/login){: external}.

	After you log in, the {{site.data.keyword.cloud_notm}} UI opens.

2. Go to the menu icon ![menu icon](../icons/icon_hamburger.svg) &gt; **Observability** to access the *Observability* Dashboard.

3. Click **Logging**. The list of logging instances is displayed.

4. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) next to the instance that you want to delete.  

5. Click **Delete**.


## Removing an instance through the CLI
{: #remove_cli}

To remove an instance of {{site.data.keyword.la_full_notm}} through the command line, complete the following steps:

1. [Pre-requisite] Installion of the {{site.data.keyword.cloud_notm}} CLI.

   For more information, see [Installing the {{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-install-ibmcloud-cli).

2. Log in to the region in the {{site.data.keyword.cloud_notm}} where you want to provision the instance. Run the following command: [ibmcloud login](/docs/cli?topic=cli-ibmcloud_cli#ibmcloud_login)

3. Set the resource group where the instance is provisioned. Run the following command: [ibmcloud target](/docs/cli?topic=cli-ibmcloud_cli#ibmcloud_target)

    By default, the *default* resource group is set.

4. Remove the instance. Run the [ibmcloud resource service-instance-delete](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_delete) command:

    ```
    ibmcloud resource service-instance-delete NAME 
    ```
    {: codeblock}

    Where NAME is the name of the instance.

    For example, to remove an instance, run the following command:

    ```
    ibmcloud resource service-instance-delete logging-instance-01
    ```
    {: codeblock}



