---
description: De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro's.
solution: Experience Manager
title: Afbeeldingscatalogi
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Afbeeldingscatalogi{#image-catalogs}

De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro&#39;s.

Ze wijzen afbeeldings- en statische inhoudsidentiteiten toe die worden gebruikt in aanvragen voor feitelijke bestandspaden, slaan verschillende metagegevens voor afbeeldingen op, zoals afbeeldingen met hyperlinks, en bieden containers voor sjablonen en afbeeldingssets.

De catalogi van het beeld worden betreden slechts door de Server van het Platform, nooit door de Server van het Beeld. Kenmerkbestanden van catalogi moeten het achtervoegsel .ini hebben en in de catalogusmap van de server van het Platform ( `PS::CatalogFolder`) worden geplaatst. Ten minste de standaardafbeeldingscatalogus is vereist en moet worden gevuld met alle kenmerken voor een correcte werking van de Platform Server.
