---
description: IS servers kunnen worden gevormd om over te slaan aan afwisselende servers voor verzoeken die een bronbeeld impliceren dat niet kan worden geopend of met succes kunnen worden gelezen.
solution: Experience Manager
title: Omleiden bij fout
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
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

De omleiding van de fout gebeurt in geen enkel ander geval.

Wanneer toegelaten en wanneer zulk een fout tijdens de verwerking van het verzoek voorkomt, verzendt de primaire server het verzoek naar de secundaire server voor verwerking. De reactie, ongeacht of het op succes of mislukking wijst, wordt dan door:sturen direct aan de cliënt. De primaire servermarkeringen logboekingangen van dergelijke door:sturen verzoeken met geheim voorgeheugengebruik `REMOTE`. De reactiegegevens worden niet lokaal door de primaire server in de cache geplaatst.

Omleiden van fout is ingeschakeld door instellen `PS::errorRedirect.rootUrl` aan de het domeinnaam en havenaantal van HTTP van de secundaire server. Bovendien wordt de verbindingstijd gevormd met `PS::errorRedirect.connectTimeout` en de maximumtijd de primaire server wacht op een reactie van de secundaire server alvorens een fout aan de cliënt terug te keren wordt gevormd met `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Als de secundaire server niet kan worden gecontacteerd, wordt een reactie van de tekstfout teruggekeerd aan de cliënt, zelfs als een standaardbeeld of een foutenbeeld wordt gevormd.

>[!NOTE]
>
>Pijptekens (|) in het nettopad worden niet ondersteund voor het omleiden van fouten.

## Zie ook {#section-2e8bfc128b944baf8108279d16492f3f}

[Omleiding fout](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
