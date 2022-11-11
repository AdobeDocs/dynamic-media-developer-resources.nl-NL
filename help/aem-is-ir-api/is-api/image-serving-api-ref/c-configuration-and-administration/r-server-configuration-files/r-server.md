---
description: Bevat instellingen voor platformservers.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

Bevat instellingen voor platformservers.

Wanneer u dit XML-bestand wijzigt, moet u ervoor zorgen dat de geldige XML-syntaxis behouden blijft, anders moet u [!DNL Platform Server] kan niet starten.

Voor wijzigingen die van kracht worden, [!DNL Platform Server] moet na het bewerken van dit bestand opnieuw worden gestart.

In het volgende diagram ziet u welke instellingen in dit bestand kunnen worden gewijzigd. Raadpleeg de desbetreffende secties eerder in dit document voor een beschrijving van deze instellingen. Merk op dat dit diagram geen volledige vertegenwoordiging van is [!DNL server.xml].

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
