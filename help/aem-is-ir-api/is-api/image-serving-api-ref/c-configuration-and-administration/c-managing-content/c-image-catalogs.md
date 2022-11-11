---
description: De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro's.
solution: Experience Manager
title: Afbeeldingscatalogi
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Afbeeldingscatalogi{#image-catalogs}

De catalogi van het beeld verstrekken vele montages van de serverconfiguratie, evenals doopvonten, ICC profielen, bevelmacro&#39;s.

Ze wijzen afbeeldings- en statische inhoudsidentiteiten toe die worden gebruikt in aanvragen voor feitelijke bestandspaden, slaan verschillende metagegevens voor afbeeldingen op, zoals afbeeldingen met hyperlinks, en bieden containers voor sjablonen en afbeeldingssets.

De catalogi van het beeld worden betreden slechts door [!DNL Platform Server], nooit door de server van het Beeld. Bestanden met cataloguskenmerken moeten het achtervoegsel .ini hebben en in het dialoogvenster [!DNL Platform Server]Catalogusmap van het type ( `PS::CatalogFolder`). Ten minste de standaardafbeeldingscatalogus is vereist en moet zijn gevuld met alle kenmerken voor een correcte werking van de component [!DNL Platform Server].
