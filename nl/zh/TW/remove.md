---

copyright:
  years:  2018, 2019
lastupdated: "2019-03-06"

keywords: LogDNA, IBM, Log Analysis, logging instance, delete

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

# 移除實例
{: #remove}

您可以從 {{site.data.keyword.Bluemix}} 使用者介面或透過指令行來移除 {{site.data.keyword.la_full_notm}} 服務的實例。
{:shortdesc}

當您從 {{site.data.keyword.cloud_notm}} 移除實例時，請完成下列作業以進行清除：

1. 寫下來源清單，該來源將度量轉遞至您要移除的 {{site.data.keyword.la_full_notm}} 實例。您必須從每一個來源中移除 LogDNA 代理程式。
2. 移除授與使用者以使用該實例的許可權。 

    如果您利用專用存取群組來管理存取權，以使用特定的實例，則必須移除這些存取群組。

    如果您使用存取群組來管理對多個記載實例的存取權，則必須移除針對您要移除之實例授與許可權的原則。
    
    如果您將個別原則授與使用者，則必須收集有權使用該實例的使用者清單。然後，針對您識別的每一位使用者，您必須移除與要刪除之實例相關的原則。


然後，從「{{site.data.keyword.cloud_notm}} 儀表板」中刪除該實例。


## 透過 {{site.data.keyword.cloud_notm}} 使用者介面移除實例
{: #remove_ui}

若要使用 {{site.data.keyword.cloud_notm}} 使用者介面來移除 {{site.data.keyword.la_full_notm}} 的實例，請完成下列步驟：

1. 登入您的 {{site.data.keyword.cloud_notm}} 帳戶。

    按一下 [{{site.data.keyword.cloud_notm}} 儀表板 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/login){:new_window}，以啟動 {{site.data.keyword.cloud_notm}} 儀表板。

	使用您的使用者 ID 和密碼登入之後，即會開啟 {{site.data.keyword.cloud_notm}} 使用者介面。

2. 移至功能表圖示 ![功能表圖示](../../icons/icon_hamburger.svg) &gt; **觀察**，以存取「*觀察* 儀表板」。

3. 選取**記載**。即會顯示記載實例的清單。

4. 選取您要刪除的實例。

5. 從*動作* 功能表中，選取**移除**。


## 透過 CLI 移除實例
{: #remove_cli}

若要透過指令行來移除 {{site.data.keyword.la_full_notm}} 的實例，請完成下列步驟：

1. [必要條件] 安裝 {{site.data.keyword.cloud_notm}} CLI。

   如需相關資訊，請參閱[安裝 {{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cloud-cli-ibmcloud-cli#ibmcloud-cli)。

   如果已安裝 CLI，請繼續進行下一步。

2. 登入 {{site.data.keyword.cloud_notm}} 中要佈建實例的地區。執行下列指令：[`ibmcloud login`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli#ibmcloud_login)

3. 設定在其中佈建實例的資源群組。執行下列指令：[`ibmcloud target`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli#ibmcloud_target)

    依預設，會設定 *default* 資源群組。

4. 移除實例。執行 [`ibmcloud resource service-instance-delete`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_delete) 指令：

    ```
    ibmcloud resource service-instance-delete NAME 
    ```
    {: codeblock}

    其中，NAME 是實例的名稱。

    例如，若要移除實例，請執行下列指令：

    ```
    ibmcloud resource service-instance-delete logdna-instance-01
    ```
    {: codeblock}



