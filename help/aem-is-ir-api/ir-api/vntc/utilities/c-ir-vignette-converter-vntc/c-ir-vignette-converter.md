---
title: Vignetconverter
description: De Vignet Converter (vntc) is een opdrachtregelprogramma voor het voorbereiden van inhoud die is gemaakt met het ontwerpen van afbeeldingen en die kan worden geïmplementeerd met behulp van Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Vignetconverter{#vignette-converter}

De Vignet Converter (vntc) is een opdrachtregelprogramma voor het voorbereiden van inhoud die is gemaakt met het ontwerpen van afbeeldingen en die kan worden geïmplementeerd met behulp van Image Rendering.

[!DNL vntc] bevindt zich in [!DNL *[!DNL install_root]*\ImageServing\bin]. Het heeft de volgende mogelijkheden:

* Hiermee zet u primaire vignetten om in vignetten met één resolutie, meerdere resoluties of piramideproductie (zie [Vignet schalen](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produceert productiekast en vensterbeklede stijldossiers (zie `-resolution` en `-jpegquality`).

* Verschillende bestandsversies van vignetten, kabinetten en Window coverings-stijlbestanden produceren voor gebruik met oudere versies van Afbeelding renderen.
* Hiermee worden weergaveafbeeldingen opgehaald uit vignetten, met volledige resolutie of als miniaturen (zie `-thumbwidth` en `-image`).
* Extraheert relevante eigenschappen uit het bronbestand (zie `-info`) en deze naar `stdout` of een optioneel logbestand (zie `-log`).

Terwijl [!DNL vntc] is optioneel, raadt Adobe aan het te gebruiken voor de beste serverprestaties. De Vignetconverter voert ook uitgebreide foutcontrole uit en kan ernstige serverproblemen, waaronder vastlopen, voorkomen wanneer deze zorgvuldig worden gebruikt.

Bij het genereren van productievensters wordt de pixelbreedte van het uitvoervignet (of 0 als piramide- of multiresolutievensters) toegevoegd aan de naam van het gegenereerde uitvoervignetbestand. Bij het verwerken van CAB-stijlbestanden wordt de uitvoerresolutie toegevoegd aan de naam van het uitvoerbestand. Alle uitvoerbestanden, inclusief de optionele miniatuur-, afbeeldings- en logbestanden en het productievignet- of kabinetsstijlbestand worden in dezelfde map geplaatst *[!DNL sourceFile]* is gevestigd (tenzij `-destPath` is opgegeven).

De Vignetconverter beperkt zichzelf standaard tot maximaal 3 GB geheugen. Wanneer vntc deze limiet bereikt, wordt de verwerking gestopt en wordt een fout gegenereerd. Deze limiet kan worden gewijzigd met `-maxmem`.

>[!NOTE]
>
>Het gereedschap Vignet bijwerken in het ontwerpen van afbeeldingen kan ook worden gebruikt om vignetten voor te bereiden voor het renderen van afbeeldingen. Met het gereedschap Inhoud ontwerpen kunt u ook bestanden in de stijl van een kast genereren voor gebruik met het renderen van afbeeldingen. Gebruiken [!DNL vntc] als de verwerking moet worden geautomatiseerd. De hulpmiddelen in het Authoring van afbeeldingen omvatten een grafische gebruikersinterface en zijn daarom doorgaans gemakkelijker interactief te gebruiken.

## Zie ook {#section-3c756bf17b634543904fdd928adeafb2}

Documentatie over het maken van afbeeldingen
