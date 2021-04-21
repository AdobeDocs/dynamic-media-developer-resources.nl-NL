---
description: Bevat instellingen voor platformservers.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
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

