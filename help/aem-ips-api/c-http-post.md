---
description: Het uploaden van activa in het Systeem van de Productie Scene7 impliceert één of meerdere POST van HTTP- verzoeken die opstelling een baan om alle logboekactiviteit te coördineren verbonden aan de geuploade dossiers.
seo-description: Het uploaden van activa in het Systeem van de Productie Scene7 impliceert één of meerdere POST van HTTP- verzoeken die opstelling een baan om alle logboekactiviteit te coördineren verbonden aan de geuploade dossiers.
seo-title: Elementen uploaden via HTTP POST's naar de UploadFile-server
solution: Experience Manager
title: Elementen uploaden via HTTP POST's naar de UploadFile-server
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# Elementen uploaden via HTTP POST&#39;s naar de UploadFile-server{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Het uploaden van activa in het Systeem van de Productie Scene7 impliceert één of meerdere POST van HTTP- verzoeken die opstelling een baan om alle logboekactiviteit te coördineren verbonden aan de geuploade dossiers.

Gebruik de volgende URL om toegang te krijgen tot de UploadFile-server:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alle POST-aanvragen voor een uploadtaak moeten afkomstig zijn van hetzelfde IP-adres.

**Toegang tot URL&#39;s voor Scene7-gebieden**

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

De uploadtaak bestaat uit een of meer HTTP POST&#39;s die een gemeenschappelijke functie gebruiken `jobHandle` om de verwerking in dezelfde taak te correleren. Elk verzoek wordt `multipart/form-data` gecodeerd en bestaat uit de volgende formulieronderdelen:

>[!NOTE]
>
>Alle POST-aanvragen voor een uploadtaak moeten afkomstig zijn van hetzelfde IP-adres.

| HTTP POST-onderdeel | Beschrijving ||-|-||`auth`| Vereist. Een XML authHeader-document waarin verificatie- en clientgegevens zijn opgegeven. Zie **Autorisatie** aanvragen onder [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Optioneel. Bij elke POST-aanvraag kunt u een of meer bestanden opnemen die u wilt uploaden. Elk dossierdeel kan filename parameter in de inhoud-plaats kopbal omvatten die als doelfilename in IPS wordt gebruikt als geen parameter wordt gespecificeerd. `uploadPostParams/fileName` |

| HTTP POST-onderdeel | uploadPostParams-elementnaam | Type | Beschrijving ||-|-|-|-|-|-|`uploadParams` (Vereist. Een XML- `uploadParams` document met de uploadparameters) | `companyHandle`|`xsd:string`| Vereist. Verwerk het bedrijf waarnaar het bestand wordt geüpload. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`jobName`|`xsd:string`| `jobName` of `jobHandle` is vereist. Naam van de uploadtaak. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`jobHandle`|`xsd:string`| `jobName` of `jobHandle` is vereist. Afhandeling van een uploadtaak die in een vorige aanvraag is gestart. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`locale`|`xsd:string`| Optioneel. Taal- en landcode voor lokalisatie. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`description`|`xsd:string`| Optioneel. Beschrijving van de taak. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`destFolder`|`xsd:string`| Optioneel. Doelmappad naar voorvoegsel voor een bestandseigenschap, met name voor browsers en andere clients die mogelijk geen volledige paden in een bestandsnaam ondersteunen. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`fileName`|`xsd:string`| Optioneel. Naam van het doelbestand. Hiermee wordt de eigenschap filename genegeerd. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`endJob`|`xsd:boolean`| Optioneel. De standaardwaarde is false. ||`uploadParams` (Vereist. Een XML- `uploadParams` document waarin de uploadparameters worden opgegeven)|`uploadParams`|`types:UploadPostJob`| Optioneel als dit een volgende aanvraag voor een bestaande actieve taak is. Als er een bestaande taak is, `uploadParams` wordt deze genegeerd en worden de bestaande taakuploadparameters gebruikt. Zie [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Binnen het `<uploadPostParams>` blok bevindt zich het `<uploadParams>` blok dat de verwerking van de opgenomen bestanden aangeeft.

Zie [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Hoewel u zou kunnen veronderstellen dat de `uploadParams` parameter voor individuele dossiers als deel van de zelfde baan kan veranderen, is dat niet het geval. Gebruik dezelfde `uploadParams` parameters voor de gehele taak.

In de eerste POST-aanvraag voor een nieuwe uploadtaak moet de `jobName` parameter worden opgegeven, bij voorkeur met een unieke taaknaam om de opiniepeiling van de taakstatus en query&#39;s voor het taaklogboek te vereenvoudigen. De extra POST- verzoeken voor de zelfde uploadbaan zouden de `jobHandle` parameter in plaats van `jobName`, gebruikend de `jobHandle` waarde moeten specificeren die van het aanvankelijke verzoek is teruggekeerd.

De laatste POST-aanvraag voor een uploadtaak moet de `endJob` parameter instellen op true, zodat er voor deze taak geen toekomstige bestanden POSTed worden. Hierdoor kan de taak direct worden voltooid nadat alle POST-bestanden zijn ingepakt. Anders loopt de taak uit als er binnen 30 minuten geen aanvullende POST-aanvragen zijn ontvangen.

## UploadPOST-reactie {#section-421df5cc04d44e23a464059aad86d64e}

Voor een succesvol POST-verzoek is de hoofdtekst van de reactie een XML- `uploadPostReturn` document, zoals de XSD in het volgende specificeert:

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

De `jobHandle` geretourneerde waarde wordt doorgegeven in de parameter `uploadPostParams`/ `jobHandle` voor alle volgende POST-aanvragen voor dezelfde taak. U kunt deze ook gebruiken om de taakstatus met de `getActiveJobs` bewerking te opiniepeilen of om de taaklogbestanden met de `getJobLogDetails` bewerking op te vragen.

Als er een fout optreedt bij het verwerken van de POST-aanvraag, bestaat de responstekst uit een van de API-fouttypen zoals beschreven in [Fouten](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Voorbeeld POST-aanvraag {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## Voorbeeld van POST-respons - geslaagd {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## Voorbeeld POST-reactie - fout {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

