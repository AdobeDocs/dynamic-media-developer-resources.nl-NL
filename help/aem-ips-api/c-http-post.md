---
description: Bij het uploaden van elementen naar Scene7 Production System worden een of meer HTTP-POSTEN gevraagd die een taak hebben ingesteld om alle logactiviteiten te coördineren die aan de geüploade bestanden zijn gekoppeld.
seo-description: Bij het uploaden van elementen naar Scene7 Production System worden een of meer HTTP-POSTEN gevraagd die een taak hebben ingesteld om alle logactiviteiten te coördineren die aan de geüploade bestanden zijn gekoppeld.
seo-title: Elementen uploaden via HTTP POST's naar de UploadFile-server
solution: Experience Manager
title: Elementen uploaden via HTTP POST's naar de UploadFile-server
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---


# Elementen uploaden via HTTP POST&#39;s naar de UploadFile-server{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Bij het uploaden van elementen naar Scene7 Production System worden een of meer HTTP-POSTEN gevraagd die een taak hebben ingesteld om alle logactiviteiten te coördineren die aan de geüploade bestanden zijn gekoppeld.

Gebruik de volgende URL om toegang te krijgen tot de UploadFile-server:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alle verzoeken van de POST om een uploadbaan moeten van het zelfde IP adres voortkomen.

**Toegang tot URL&#39;s voor Scene7-regio&#39;s**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geografische locatie </p> </th> 
   <th colname="col2" class="entry"> <p>Productie-URL </p> </th> 
   <th colname="col3" class="entry"> <p>Staging-URL (gebruik voor ontwikkeling en testen voorafgaand aan de productie) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Noord-Amerika </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Midden-Oosten, Azië </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Azië Stille Oceaan </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Workflow van de uploadtaak {#section-873625b9512f477c992f5cdd77267094}

De uploadtaak bestaat uit een of meer HTTP POST&#39;s die een gemeenschappelijke `jobHandle` gebruiken om de verwerking in dezelfde taak te correleren. Elk verzoek is `multipart/form-data` gecodeerd en bestaat uit de volgende formulieronderdelen:

>[!NOTE]
>
>Alle verzoeken van de POST om een uploadbaan moeten van het zelfde IP adres voortkomen.

| HTTP-POST maakt deel uit van | Beschrijving |
|-|-|
|`auth` |  Vereist. Een XML authHeader-document waarin verificatie- en clientgegevens zijn opgegeven. Zie **Verificatie aanvragen** onder [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Optioneel. U kunt een of meer bestanden opnemen om te uploaden bij elke aanvraag van een POST. Elk dossierdeel kan filename parameter in de inhoud-plaats kopbal omvatten die als doelfilename in IPS wordt gebruikt als geen `uploadPostParams/fileName` parameter wordt gespecificeerd. |

| HTTP-POST maakt deel uit  | naam van uploadPostParams-element  | Type  | Beschrijving  |
|-|-|-|-|-|-|
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)  |  `companyHandle` | `xsd:string` | Vereist. Verwerk het bedrijf waarnaar het bestand wordt geüpload. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`jobName` | `xsd:string` | Of `jobName` of `jobHandle` is vereist. Naam van de uploadtaak. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`jobHandle` | `xsd:string` | Of `jobName` of `jobHandle` is vereist. Afhandeling van een uploadtaak die in een vorige aanvraag is gestart. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`locale` | `xsd:string` | Optioneel. Taal- en landcode voor lokalisatie. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`description` | `xsd:string` | Optioneel. Beschrijving van de taak. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`destFolder` | `xsd:string` | Optioneel. Doelmappad naar voorvoegsel voor een bestandseigenschap, met name voor browsers en andere clients die mogelijk geen volledige paden in een bestandsnaam ondersteunen. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`fileName` | `xsd:string` | Optioneel. Naam van het doelbestand. Hiermee wordt de eigenschap filename genegeerd. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`endJob` | `xsd:boolean` | Optioneel. De standaardwaarde is false. |
|`uploadParams` (Vereist. Een XML `uploadParams`-document dat de uploadparameters opgeeft)|`uploadParams` | `types:UploadPostJob` | Optioneel als dit een volgende aanvraag voor een bestaande actieve taak is. Als er een bestaande taak is, wordt `uploadParams` genegeerd en worden de bestaande taakuploadparameters gebruikt. Zie [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Binnen het `<uploadPostParams>` blok is het `<uploadParams>` blok dat de verwerking van de inbegrepen dossiers aanwijst.

Zie [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Hoewel u zou kunnen veronderstellen dat de `uploadParams` parameter voor individuele dossiers als deel van de zelfde baan kan veranderen, is dat niet het geval. Gebruik dezelfde parameters `uploadParams` voor de gehele taak.

In het initiële verzoek van de POST voor een nieuwe uploadtaak moet de parameter `jobName` worden opgegeven, bij voorkeur met een unieke taaknaam om de opiniepeiling van de taakstatus en query&#39;s voor het taaklogboek te vereenvoudigen. Aanvullende aanvragen voor POSTEN voor dezelfde uploadtaak moeten de `jobHandle`-parameter opgeven in plaats van `jobName`, waarbij de `jobHandle`-waarde wordt gebruikt die door de oorspronkelijke aanvraag is geretourneerd.

De laatste aanvraag voor een POST voor een uploadtaak moet de parameter `endJob` op true instellen, zodat er geen toekomstige bestanden voor deze taak worden gePOST. Hierdoor kan de taak direct worden voltooid nadat alle POST-bestanden zijn ingepakt. Anders wordt de taak beëindigd als er binnen 30 minuten geen verzoeken om extra POSTEN zijn ontvangen.

## UploadPOST-reactie {#section-421df5cc04d44e23a464059aad86d64e}

Voor een succesvol verzoek van de POST, zal het antwoordlichaam een document van XML `uploadPostReturn` zijn, zoals XSD in het volgende specificeert:

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

De geretourneerde `jobHandle` wordt doorgegeven in de parameter `uploadPostParams`/ `jobHandle` voor alle volgende aanvragen voor POSTEN voor dezelfde taak. U kunt deze ook gebruiken om de taakstatus te opiniepeilen met de bewerking `getActiveJobs` of om de taaklogbestanden op te vragen met de bewerking `getJobLogDetails`.

Als er een fout is die het verzoek van de POST verwerkt, bestaat de reactiekarakter uit één van de API foutentypes zoals die in [Faults](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b) worden beschreven.

## Voorbeeld POST request {#section-810fe32abdb9426ba0fea488dffadd1e}

```
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Respons van de POST van het voorbeeld - succes {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Respons POST voorbeeld - fout {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

