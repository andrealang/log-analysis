---

copyright:
  years:  2018, 2019
lastupdated: "2019-08-12"

keywords: LogDNA, IBM, Log Analysis, logging, overview

subcollection: LogDNA

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

# Managing logs for HIPAA resources
{: #manage_hipaa_logs}

Across every industry, organizations require tighter controls and visibility into where their data is stored and processed in the {{site.data.keyword.cloud}}. To manage logs that are generated in your **EU-supported account** by using the {{site.data.keyword.la_full_notm}} service, consider the following information:
{:shortdesc}



# Enabling EU and HIPAA supported settings
{: #eu-hipaa-supported}

If you're the account owner, you can enable your {{site.data.keyword.cloud}} account to be EU supported and HIPAA supported. You might choose to enable the EU Supported setting, for example, if you use resources to process personal data for European citizens. And you might choose to enable the HIPAA Supported setting if you plan to include Protected Health Information (PHI) in HIPAA-enabled services.
{:shortdesc}


## Enabling the EU Supported setting
{: #bill_eusupported}

Enabling the EU supported setting limits Advanced Customer Support (ACS) that is provided by {{site.data.keyword.Bluemix_notm}} support team members in the European Union region. However, {{site.data.keyword.Bluemix_notm}} processing activities might be performed by teams that are outside of the EU region. Global teams can be contacted when issues aren't resolved by the ACS teams in the EU. The global teams are always contacted at the instruction of the EU support team and only when there's no impact to the security or privacy of your data.

By enabling this setting, EU supported services have strict access controls to ensure the data you store and process is restricted and controlled by the IBM support team in the EU region. If {{site.data.keyword.Bluemix_notm}} experts that are outside of the European region need access to this data, an EU support team member reviews the access request. The EU support team member provides necessary access to the global cloud expert only to the requested system, and only for a specific time frame after which access is revoked. Throughout this process, your data is always protected.

  1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage > Account**, and select **Account settings**.
  2. Click **On**.
  3. Read the information about enabling the setting, and select **I understand and agree to these terms**.
  4. Click **On**.

   After you enable the EU Supported setting, you can use the EU Supported tag to search the catalog for offerings that have EU-supported plans. See [Requesting support for resources in the European Union](/docs/get-support?topic=get-support-getting-customer-support#eusupported) for more information.


## Enabling the HIPAA Supported setting
{: #enabling-hipaa}

The US Health Insurance Portability and Accountability Act (HIPAA) and the Health Information Technology for Economic and Clinical Health (HITECH) Act define standards for handling electronic healthcare transactions and information. If you or your company is a covered entity as defined by HIPAA, you must enable the HIPAA Supported setting if you run sensitive workloads that are regulated under HIPAA and the HITECH Act. Learn more about {{site.data.keyword.Bluemix_notm}} compliance in [Compliance on the {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud/compliance){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon").

Enabling this setting has the following effects:

* Enables you to filter on HIPAA Enabled services in the catalog
* Indicates to IBM that your account stores protected health information (PHI)
* Digitally accepts the IBM Business Associate Addendum (BAA) for covered entities

Enable this setting only if you or your company is a covered entity as defined by HIPAA. If you or your company is a business associate of a covered entity, [contact {{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-wcp){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon") to accept the applicable BAA. For more information about HIPAA definitions of covered entities and business associates, see the [US Department of Health & Human Services](https://www.hhs.gov/hipaa/for-professionals/covered-entities/index.html){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon") website.
{: important}

Accounts that enable the HIPAA Supported setting still have access to the full catalog of services. {{site.data.keyword.Bluemix_notm}} ser


###  Label your service
{: #hipaa_tag}


Setting the HIPAA tag for
As a service owner you can use the following steps to set the HIPAA tag for deployments that are HIPAA-specific.

1. Go to the [Global catalog](https://globalcatalog.cloud.ibm.com/search) and log in.
2. Search for your service, and select it.
3. Go to the deployments section of your service by going to **Service** &gt; **Plan** &gt; **Deployment**. The deployments 
(for example, Standard @ US South) need to have the tag applied if they are HIPAA-specific.
4. Select the **Tags** tab and verify that you have permission to tag the deployment. You will see a field to add a tag and when you do then you are able to save the changes.
5. Tag the appropriate deployments with `HIPAA` and save the service entry.

When the `HIPAA` tag is set, you can verify that the tag is reflected in the catalog UI by selecting a HIPAA supported account and filtering the [catalog](cloud.ibm.com/catalog) with the `HIPAA` filter.
vices typically offer multiple plans. The HIPAA Enabled label on a service can apply to all available plans or be limited to specific plans or configurations. You as the client are solely responsible for limiting PHI to HIPAA Enabled offering plans and architecting in accordance with HIPAA and HITECH.

1. Go to **Manage > Account**, and select **Account setting** in the console.
2. For the HIPAA Supported option, click **On**.
3. Read the information about enabling this setting.

  You can't disable the setting after you enable it.
  {: note}

4. Select **Accept**, and click **Submit**.

  After you enable the HIPAA Supported setting, you can use the HIPAA Enabled tag to search the catalog for offerings that are HIPAA enabled.
