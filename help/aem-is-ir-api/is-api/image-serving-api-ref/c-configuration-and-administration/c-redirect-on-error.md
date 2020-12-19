---
description: IS servers kunnen worden gevormd om over te slaan aan afwisselende servers voor verzoeken die een bronbeeld impliceren dat niet kan worden geopend of met succes kunnen worden gelezen.
seo-description: IS servers kunnen worden gevormd om over te slaan aan afwisselende servers voor verzoeken die een bronbeeld impliceren dat niet kan worden geopend of met succes kunnen worden gelezen.
seo-title: Omleiden bij fout
solution: Experience Manager
title: Omleiden bij fout
topic: Scene7 Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# Omleiden bij fout{#redirect-on-error}

IS servers kunnen worden gevormd om over te slaan aan afwisselende servers voor verzoeken die een bronbeeld impliceren dat niet kan worden geopend of met succes kunnen worden gelezen.

De volgende typen verzoeken worden omgeleid:

* IS Afbeeldingen die zich in de catalogus bevinden, maar niet op schijf.

   Als een afbeelding zich niet in een catalogus bevindt, kan een fout bij het omleiden niet optreden als de afbeelding niet is gevonden.

* Beschadigde afbeeldingen, kleurprofielen of lettertypen.
* Statische inhoud kan niet worden gevonden op schijf.

   Aanvragen voor statische inhoud worden omgeleid wanneer deze niet op schijf kan worden gevonden, zelfs als de statische inhoud waarnaar wordt verwezen geen catalogusrecord heeft.

De omleiding van de fout zal in geen ander geval gebeuren.

Wanneer toegelaten en wanneer zulk een fout tijdens de verwerking van het verzoek voorkomt, zal de primaire server het verzoek naar de secundaire server voor verwerking verzenden. De reactie, ongeacht of het op succes of mislukking wijst, wordt dan door:sturen direct aan de cliënt. De primaire server markeert logboekingangen van dergelijke door:sturen verzoeken met geheim voorgeheugengebruik `REMOTE`. De reactiegegevens worden niet lokaal door de primaire server in de cache geplaatst.

De omleiding van de fout wordt toegelaten door `PS::errorRedirect.rootUrl` aan de het domeinnaam en havenaantal van HTTP van de secundaire server te plaatsen. Daarnaast wordt de time-out van de verbinding geconfigureerd met `PS::errorRedirect.connectTimeout` en wordt de maximale tijd die de primaire server wacht op een reactie van de secundaire server voordat een fout naar de client wordt geretourneerd, geconfigureerd met `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Als de secundaire server niet kan worden gecontacteerd, zal een reactie van de tekstfout aan de cliënt worden teruggekeerd, zelfs als een standaardbeeld of een foutenbeeld wordt gevormd.

>[!NOTE]
>
>Pijptekens (|) in het nettopad worden niet ondersteund voor het omleiden van fouten.

## Zie ook {#section-2e8bfc128b944baf8108279d16492f3f}

[Omleiding fout](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
