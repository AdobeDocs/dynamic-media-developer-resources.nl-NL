---
description: De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro's.
seo-description: De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro's.
seo-title: Afbeeldingscatalogi
solution: Experience Manager
title: Afbeeldingscatalogi
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Afbeeldingscatalogi{#image-catalogs}

De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro&#39;s.

Ze wijzen afbeeldings- en statische inhoudsidentiteiten toe die worden gebruikt in aanvragen voor feitelijke bestandspaden, slaan verschillende metagegevens voor afbeeldingen op, zoals afbeeldingen met hyperlinks, en bieden containers voor sjablonen en afbeeldingssets.

De catalogi van het beeld worden betreden slechts door de Server van het Platform, nooit door de Server van het Beeld. Kenmerkbestanden van catalogi moeten het achtervoegsel .ini hebben en in de catalogusmap van de server van het Platform ( `PS::CatalogFolder`) worden geplaatst. Ten minste de standaardafbeeldingscatalogus is vereist en moet worden gevuld met alle kenmerken voor een correcte werking van de Platform Server.
