---
description: In dit onderwerp wordt de syntaxis voor vntc-gebruik beschreven.
solution: Experience Manager
title: Gebruik
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# Gebruik{#usage}

In dit onderwerp wordt de syntaxis voor vntc-gebruik beschreven.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* Dit is het pad en de naam van het bestand dat moet worden verwerkt. Dit kan een pad zijn dat relatief is ten opzichte van de huidige werkmap of een absoluut pad. Dit moet een geldig vignet-, kabinetstijl- of vensterdekkend stijlbestand zijn en een van de volgende achtervoegsels hebben: [!DNL .vnt], [!DNL .vnc], of [!DNL .vnw]. Vereist.

*[!DNL destFile]* Dit is het pad en de naam voor het uitvoervignetbestand. Indien niet opgegeven, wordt het uitvoerbestand in de map geplaatst die is opgegeven met `-destpath`. In dit scenario wordt de bestandsnaam automatisch gegenereerd op basis van de naam van het invoerbestand en een achtervoegsel voor de grootte, gescheiden met de tekenreeks die met `-separator`. Voor vignetten is het grootteachtervoegsel de pixelbreedte van het uitvoervignet met één resolutie, de breedte van de eerste weergave van een uitvoervignet met meerdere resoluties, of &#39;0&#39; in het geval van een piramidevignet. Voor kabinetsstijlbestanden wordt de uitvoerresolutie gebruikt als achtervoegsel van het bestand. *[!DNL destFile]* wordt genegeerd wanneer `-info` wordt opgegeven.
