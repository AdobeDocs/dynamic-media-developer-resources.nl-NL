---
title: Elementen uploaden via HTTP POST's naar de UploadFile-server
description: Elementen uploaden naar [!DNL Dynamic Media] Klassiek omvat één of meerdere verzoeken van de POST van HTTP dat opstelling een baan om alle logboekactiviteit te coördineren verbonden aan de geupload dossiers.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Elementen uploaden via HTTP POST&#39;s naar de UploadFile-server{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Bij het uploaden van middelen naar Dynamic Media Classic zijn een of meer HTTP-POSTEN vereist die een taak instellen om alle logactiviteiten te coördineren die aan de geüploade bestanden zijn gekoppeld.

Gebruik de volgende URL om toegang te krijgen tot de UploadFile-server:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alle verzoeken van de POST om een uploadbaan moeten van het zelfde IP adres voortkomen.

**Toegang tot URL&#39;s voor Dynamic Media-regio&#39;s**

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

De uploadtaak bestaat uit een of meer HTTP POST&#39;s die een gemeenschappelijke `jobHandle` om de verwerking tot dezelfde taak te correleren. Elke aanvraag is `multipart/form-data` gecodeerd en bestaat uit de volgende formulieronderdelen:

>[!NOTE]
>
>Alle verzoeken van de POST om een uploadbaan moeten van het zelfde IP adres voortkomen.

|  HTTP-POST maakt deel uit van  |  Beschrijving  |
|---|---|
| `auth`  |   Vereist. Een XML authHeader-document waarin verificatie- en clientgegevens zijn opgegeven. Zie **Verificatie aanvragen** krachtens [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Optioneel. U kunt een of meer bestanden opnemen om te uploaden bij elke aanvraag van een POST. Elk dossierdeel kan filename parameter in de inhoud-plaats kopbal omvatten die als doelfilename in IPS wordt gebruikt als geen `uploadPostParams/fileName` parameter wordt opgegeven. |

|  HTTP-POST maakt deel uit van   |  uploadPostParams, elementnaam   |  Type   |  Beschrijving   |
|---|---|---|---|
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters)   |   `companyHandle`  |  `xsd:string`  | Vereist. Verwerk het bedrijf waarnaar het bestand wordt geüpload.  |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `jobName`  |  `xsd:string`  | Willekeurig `jobName` of `jobHandle` is vereist. Naam van de uploadtaak.  |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `jobHandle`  |  `xsd:string`  | Willekeurig `jobName` of `jobHandle` is vereist. Afhandeling van een uploadtaak die in een vorige aanvraag is gestart.  |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `locale`  |  `xsd:string`  | Optioneel. Taal- en landcode voor lokalisatie.  |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `description`  |  `xsd:string`  | Optioneel. Beschrijving van de taak.  |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `destFolder`  |  `xsd:string`  | Optioneel. Doelmappad naar voorvoegsel voor een bestandseigenschap, met name voor browsers en andere clients die mogelijk geen volledige paden in een bestandsnaam ondersteunen.  |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `fileName`  |  `xsd:string`  | Optioneel. Naam van het doelbestand. Hiermee wordt de eigenschap filename genegeerd. |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `endJob`  |  `xsd:boolean`  | Optioneel. De standaardwaarde is false. |
| `uploadParams` (Vereist. Een XML `uploadParams` document met de uploadparameters) | `uploadParams`  |  `types:UploadPostJob`  | Optioneel als dit een volgende aanvraag voor een bestaande actieve taak is. Als er een bestaande baan is, `uploadParams` wordt genegeerd en worden de bestaande taakuploadparameters gebruikt. Zie [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Binnen de `<uploadPostParams>` blok is `<uploadParams>` blok dat de verwerking van de inbegrepen dossiers aanwijst.

Zie [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Terwijl u zou kunnen veronderstellen dat `uploadParams` parameter kan voor afzonderlijke bestanden worden gewijzigd als onderdeel van dezelfde taak, dat is niet het geval. Hetzelfde gebruiken `uploadParams` parameters voor de gehele taak.

In de eerste aanvraag voor een POST voor een nieuwe uploadtaak moet de instelling `jobName` parameter, bij voorkeur met gebruik van een unieke taaknaam om de opiniepeiling van de taakstatus en query&#39;s voor het taaklogboek te vereenvoudigen. Aanvullende verzoeken om POST voor dezelfde uploadtaak moeten de instelling `jobHandle` parameter in plaats van `jobName`, met de `jobHandle` waarde die door de oorspronkelijke aanvraag wordt geretourneerd.

In het laatste verzoek om POST voor een uploadtaak moet de instelling `endJob` parameter aan waar zodat geen toekomstige dossiers POSTed voor deze baan zijn. Hierdoor kan de taak direct worden voltooid nadat alle POST-bestanden zijn ingepakt. Anders wordt de taak beëindigd als er binnen 30 minuten geen verzoeken om extra POSTEN zijn ontvangen.

## UploadPOST-reactie {#section-421df5cc04d44e23a464059aad86d64e}

Voor een succesvol verzoek van de POST, is het antwoordlichaam een XML `uploadPostReturn` document, zoals in de XSD-code hieronder wordt aangegeven:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

De `jobHandle` teruggekeerde is overgegaan in `uploadPostParams`/ `jobHandle` parameter voor alle volgende aanvragen van POSTEN voor dezelfde taak. U kunt de taakstatus ook opvragen met de `getActiveJobs` of om de taak te controleren die bij de `getJobLogDetails` bewerking.

Als er een fout optreedt bij het verwerken van het verzoek van de POST, bestaat de responsinstantie uit een van de API-fouttypen die worden beschreven in [Standaardwaarden](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Voorbeeld POST request {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
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

## Respons POST voorbeeld - succes {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
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

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
