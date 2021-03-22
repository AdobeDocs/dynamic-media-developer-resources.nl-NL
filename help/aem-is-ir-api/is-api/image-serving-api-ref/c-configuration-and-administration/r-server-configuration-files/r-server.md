---
description: Bevat instellingen voor platformservers.
seo-description: Bevat instellingen voor platformservers.
seo-title: server.xml
solution: Experience Manager
title: server.xml
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# server.xml{#server-xml}

Bevat instellingen voor platformservers.

Wanneer u dit XML-bestand wijzigt, moet u ervoor zorgen dat een geldige XML-syntaxis behouden blijft, anders start de Server van het Platform mogelijk niet.

Wijzigingen worden pas van kracht nadat de server met het Platform opnieuw is gestart nadat u dit bestand hebt bewerkt.

In het volgende diagram ziet u welke instellingen in dit bestand kunnen worden gewijzigd. Raadpleeg de desbetreffende secties eerder in dit document voor een beschrijving van deze instellingen. Merk op dat dit diagram geen volledige vertegenwoordiging van [!DNL server.xml] is.

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

