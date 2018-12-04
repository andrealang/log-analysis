---

copyright:
  years: 2018
lastupdated: "2018-12-04"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}

# Navigating to the Web UI
{: #launch}

After you provision an instance of the {{site.data.keyword.la_full_notm}} service in the {{site.data.keyword.Bluemix}}, and configure a LogDNA agent for a log data source, you can view, monitor, and manage logs through the {{site.data.keyword.la_full_notm}} web UI.
{:shortdesc}


## Granting IAM policies to a user to view data 
{: #step1}

**Note:** You must be an adminsitrator of the {{site.data.keyword.la_full_notm}} service, an administrator of an {{site.data.keyword.la_full_notm}} instance, or have account IAM permissions to grant other users policies.

The following table lists the minimum policies that a user must have to be able to launch the IBM Cloud Monitoring with Sysdig Web UI, and view data:

| Service                              | Role                      | Permission granted                                                                            |
|--------------------------------------|---------------------------|-----------------------------------------------------------------------------------------------|
| `{{site.data.keyword.la_full_notm}}` | Platform role: Viewer     | Allows the user to view the list of service instances in the Observability Logging dashboard. |
| `{{site.data.keyword.la_full_notm}}` | Service role: Writer      | Allows the user to launch the Web UI and view logs in the Web UI.                             |
{: caption="Table 1. IAM policies" caption-side="top"} 

For more information on how to configure these policies for a user, see [Granting permissions to a user to view logs](/docs/services/Log-Analysis-with-LogDNA/work_iam.html#user_logdna).


## Launching the web UI through the {{site.data.keyword.Bluemix_notm}} UI
{: #step2}

You launch the web UI within the context of an {{site.data.keyword.la_full_notm}} instance, from the {{site.data.keyword.Bluemix_notm}} UI. 

Complete the following steps to launch the web UI:

1. Log in to your {{site.data.keyword.Bluemix_notm}} account.

    The {{site.data.keyword.Bluemix_notm}} dashboard can be found at: [http://bluemix.net ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://bluemix.net){:new_window}.

	After you log in with your user ID and password, the {{site.data.keyword.Bluemix_notm}} Dashboard opens.

2. In the navigation menu, select **Observability**. 

3. Select **Logging**. 

    The list of instances that are available on {{site.data.keyword.Bluemix_notm}} is displayed.

4. Select one instance. Then, click **View LogDNA**.

The Web UI opens.


## Getting the web UI URL
{: #get}

