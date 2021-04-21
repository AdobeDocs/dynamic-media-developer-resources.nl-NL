---
description: De Vignet Converter (vntc) is een opdrachtregelprogramma waarmee u inhoud die is gemaakt met het ontwerpen van afbeeldingen, kunt voorbereiden op implementatie met behulp van Image Rendering.
solution: Experience Manager
title: Vignetconverter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Vignetconverter{#vignette-converter}

De Vignet Converter (vntc) is een opdrachtregelprogramma waarmee u inhoud die is gemaakt met het ontwerpen van afbeeldingen, kunt voorbereiden op implementatie met behulp van Image Rendering.

[!DNL vntc] bevindt zich in [!DNL  *[!DNL install_root]*\ImageServing\bin]. Het heeft de volgende mogelijkheden:

* Hiermee converteert u primaire vignetten naar één resolutie, multiresolutie of piramideproductivignetten (zie [Schalen van vignet](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produceert productiekast en venster dat stijldossiers (zie `-resolution` en `-jpegquality`) behandelt.

* Er kunnen verschillende bestandsversies van vignetten, kabinetten en vensteromslagen worden gemaakt voor gebruik met oudere versies van renderen van afbeeldingen.
* Hiermee haalt u weergaveafbeeldingen op uit vignetten, volledige resolutie of miniaturen (zie `-thumbwidth` en `-image`).
* Extraheert relevante eigenschappen uit het bronbestand (zie `-info`) en verzendt deze naar `stdout` of een optioneel logbestand (zie `-log`).

Hoewel het gebruik van [!DNL vntc] optioneel is, wordt dit ten zeerste aanbevolen voor de beste serverprestaties. [!DNL vntc] Voert ook uitgebreide fout controle uit en kan ernstige serverkwesties, met inbegrip van neerstortingen verhinderen, wanneer zorgvuldig gebruikt.

Bij het genereren van productievignetten wordt de pixelbreedte van het uitvoervignet (of 0 in het geval van piramide- of multiresolutie-vignetten) toegevoegd aan de naam van het gegenereerde uitvoervignetbestand. Bij het verwerken van CAB-stijlbestanden wordt de uitvoerresolutie toegevoegd aan de naam van het uitvoerbestand. Alle uitvoerbestanden, inclusief de optionele miniatuur-, afbeeldings- en logbestanden en het productievignet- of CAB-stijlbestand worden in dezelfde map geplaatst als *[!DNL sourceFile]* (tenzij `-destPath` is opgegeven).

[!DNL vntc] beperkt zichzelf standaard tot maximaal 3 GB geheugen. Wanneer Vntc deze limiet bereikt, wordt de verwerking gestopt en wordt een fout gegenereerd. Deze limiet kan worden gewijzigd met `-maxmem`.

>[!NOTE]
>
>Het gereedschap Vignet bijwerken in het ontwerpen van afbeeldingen kan ook worden gebruikt om vignetten voor te bereiden op het gebruik van Afbeelding renderen. Op dezelfde manier kan het gereedschap Inhoud ontwerpen ook bestanden in de kabinetsstijl genereren die kunnen worden gebruikt bij het renderen van afbeeldingen. Gebruik [!DNL vntc] als de verwerking moet worden geautomatiseerd. De hulpmiddelen in het Authoring van afbeeldingen omvatten een grafische gebruikersinterface en zijn daarom doorgaans gemakkelijker interactief te gebruiken.

## Zie ook {#section-3c756bf17b634543904fdd928adeafb2}

Documentatie over het maken van afbeeldingen
