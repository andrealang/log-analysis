---

copyright:
  years: 2017, 2019

lastupdated: "2019-03-06"

keywords: IBM Cloud, logging

subcollection: cloudloganalysis

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


# Perguntas e respostas frequentes usando a CLI do IBM Cloud
{: #cli_qa}

Aqui estão as respostas para perguntas comuns sobre como usar a CLI do {{site.data.keyword.Bluemix}} com o serviço {{site.data.keyword.loganalysisshort}}. 
{:shortdesc}

* [Como efetuar login no {{site.data.keyword.Bluemix_notm}}](/docs/services/CloudLogAnalysis/qa/cli_qa.html#login)
* [Como instalar o {{site.data.keyword.Bluemix_notm}} CLI](/docs/services/CloudLogAnalysis/qa/cli_qa.html#install_bmx_cli)
* [Como obter o GUID de uma conta](/docs/services/CloudLogAnalysis/qa/cli_qa.html#account_guid)
* [Como obter o GUID de uma organização](/docs/services/CloudLogAnalysis/qa/cli_qa.html#org_guid)
* [Como obter o GUID de um espaço](/docs/services/CloudLogAnalysis/qa/cli_qa.html#space_guid)

## Como efetuar login no IBM Cloud?
{: #login}

Execute o comando a seguir para efetuar login em uma região no {{site.data.keyword.Bluemix_notm}}, em que o serviço do {{site.data.keyword.loganalysisshort}} está disponível: 

```
ibmcloud login -a Endpoint
```
{: codeblock}
	
Em que *Endpoint* é a URL para efetuar login no {{site.data.keyword.Bluemix_notm}}. Essa URL é diferente por região.
	
<table>
    <caption>Lista de terminais para acessar o {{site.data.keyword.Bluemix_notm}}</caption>
	<tr>
	  <th>Region</th>
	  <th>URL</th>
	</tr>
	<tr>
	  <td>Alemanha</td>
	  <td>api.eu-de.bluemix.net</td>
	</tr>
	<tr>
	  <td>Sydney</td>
	  <td>api.au-syd.bluemix.net</td>
	</tr>
	<tr>
	  <td>Sul dos Estados Unidos</td>
	  <td>api.ng.bluemix.net</td>
	</tr>
	<tr>
	  <td></td>
	  <td>api.eu-gb.bluemix.net</td>
	</tr>
</table>

Por exemplo, para efetuar login na região Sul dos EUA, execute o comando a seguir:
	
```
ibmcloud login -a https://api.ng.bluemix.net
```
{: codeblock}

Siga as instruções. 

Também é possível configurar uma organização e um espaço. Execute o comando a seguir:

```
ibmcloud target -o OrgName -s SpaceName
```
{: codeblock}

Em que

* OrgName é o nome da organização.
* SpaceName é o nome do espaço.

	
	
## Como instalar a CLI do IBM Cloud?
{: #install_bmx_cli}

Consulte  [ Fazer download e instalar a  {{site.data.keyword.Bluemix}}  CLI ](/docs/cli/index.html#overview).



## Como obter o GUID de uma conta
{: #account_guid}
	
Conclua as etapas a seguir para obter o GUID de uma conta:
	
1. Efetue login em uma região no {{site.data.keyword.Bluemix_notm}}. 

    Para obter mais informações, veja [Como efetuar login no {{site.data.keyword.Bluemix_notm}}](/docs/services/CloudLogAnalysis/qa/cli_qa.html#login).
	
2. Execute o comando `ibmcloud iam accounts` para obter o GUID de uma conta.

    ```
	Contas ibmcloud iam
	```
	{: codeblock} 
	
	Por exemplo, para recuperar todas as contas com seus GUIDs correspondentes para o usuário xxx@yyy.com, execute o comando:
	
	```
	ibmcloud iam accounts
	Retrieving all accounts of xxx@yyy.com...
    OK
    Account GUID                       Name                               Type    State    Owner User ID   
    12345123451234512345123451234512   A Account                          TRIAL   ACTIVE   xxx@yyy.com   
    23456234562345622456234561234561   B Account                          TRIAL   ACTIVE   zzz@yyy.com   
	```
	{: screen}

	
## Como obter o GUID de uma organização
{: #org_guid}

Conclua as etapas a seguir para obter o GUID de uma organização:
	
1. Efetue login em uma região, uma organização e um espaço no {{site.data.keyword.Bluemix_notm}}. 

    Para obter mais informações, veja [Como efetuar login no {{site.data.keyword.Bluemix_notm}}](/docs/services/CloudLogAnalysis/qa/cli_qa.html#login).

2. Execute o comando `ibmcloud iam org` para obter o GUID da organização. 

    ```
    ibmcloud iam org NAME --guid
    ```
    {: codeblock}
	
    em que NAME é o nome da organização do {{site.data.keyword.Bluemix_notm}}.        
		
		
		
## Como obter o GUID de um espaço
{: #space_guid2}
	
Conclua as etapas a seguir para obter o GUID de um espaço:
	
1. Efetue login em uma região, uma organização e um espaço no {{site.data.keyword.Bluemix_notm}}. 

    Para obter mais informações, veja [Como efetuar login no {{site.data.keyword.Bluemix_notm}}](/docs/services/CloudLogAnalysis/qa/cli_qa.html#login).
	
2. Execute o comando `ibmcloud iam space` para obter o GUID do espaço. 

    ```
    ibmcloud iam space NAME --guid
    ```
    {: codeblock}
	
    em que NAME é o nome de um espaço do {{site.data.keyword.Bluemix_notm}}. 
	
    Por exemplo, para obter o GUID para o espaço *dev*, execute o comando a seguir:
	
    ```
    ibmcloud iam space dev --guid
    e03afff1-3456-4af6-1234-59treg1b0abc
    ```
    {: screen}




		
		
