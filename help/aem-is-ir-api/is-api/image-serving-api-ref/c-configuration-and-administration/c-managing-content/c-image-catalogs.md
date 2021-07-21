---
description: De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro's.
solution: Experience Manager
title: Afbeeldingscatalogi
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Afbeeldingscatalogi{#image-catalogs}

De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro&#39;s.

Ze wijzen afbeeldings- en statische inhoudsidentiteiten toe die worden gebruikt in aanvragen voor feitelijke bestandspaden, slaan verschillende metagegevens voor afbeeldingen op, zoals afbeeldingen met hyperlinks, en bieden containers voor sjablonen en afbeeldingssets.

De catalogi van het beeld worden betreden slechts door de Server van het Platform, nooit door de Server van het Beeld. Kenmerkbestanden van catalogi moeten het achtervoegsel .ini hebben en in de catalogusmap van de server van het Platform ( `PS::CatalogFolder`) worden geplaatst. Ten minste de standaardafbeeldingscatalogus is vereist en moet worden gevuld met alle kenmerken voor een correcte werking van de Platform Server.
