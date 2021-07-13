---
description: Deze release—Afbeelding met 6.6.1 en Afbeelding weergeven 6.6.1—vervangt de afbeelding met 6.5.3 en Afbeelding weergeven 6.5.3.
solution: Experience Manager
title: Over deze release
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Over deze release{#about-this-release}

Deze release—Afbeelding met 6.6.1 en Afbeelding weergeven 6.6.1—vervangt de afbeelding met 6.5.3 en Afbeelding weergeven 6.5.3.

## Bekende problemen en gedragswijzigingen {#section-9dbc05206187477f926a78e8108a34e1}

* Het gebruik van het vraagteken in element-id&#39;s wordt niet meer ondersteund, zelfs niet als het teken URL-gecodeerd is.
* Dynamische bannerverzoeken `/xfl/flash/` worden niet meer ondersteund en retourneren nu een http 404-foutcode.
* W2P `/is/agm/`-verzoeken worden niet meer ondersteund.
* Sommige foutberichten worden niet meer naar de browser gerenderd. Als dusdanig, moet u het spoorlogboek herzien om te zuiveren.

## Nieuwe functies {#section-b1386e36cb4544ebb79766a06b16842d}

* Slim staal
* Slim uitsnijden

## Bug Fix {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Correctie van het probleem waarbij de optie `\qc` RTF gevolgd door een spatie een verzoek deed om niet te renderen.
