---
description: In dit onderwerp wordt de syntaxis voor vntc-gebruik beschreven.
seo-description: In dit onderwerp wordt de syntaxis voor vntc-gebruik beschreven.
seo-title: Gebruik
solution: Experience Manager
title: Gebruik
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Gebruik{#usage}

In dit onderwerp wordt de syntaxis voor vntc-gebruik beschreven.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* Dit is het pad en de naam van het bestand dat moet worden verwerkt. Dit kan een pad zijn dat relatief is ten opzichte van de huidige werkmap of een absoluut pad. Dit moet een geldig vignet-, kabinetstijl- of vensterdekkend stijlbestand zijn en een van de volgende achtervoegsels hebben: [!DNL .vnt], [!DNL .vnc] of [!DNL .vnw]. Vereist.

*[!DNL destFile]* Dit is het pad en de naam voor het uitvoervignetbestand. Indien niet opgegeven, wordt het uitvoerbestand in de map geplaatst die is opgegeven met `-destpath`. In dit scenario wordt de bestandsnaam automatisch gegenereerd op basis van de naam van het invoerbestand en een achtervoegsel voor de grootte, gescheiden met de tekenreeks die met `-separator` is opgegeven. Voor vignetten is het grootteachtervoegsel de pixelbreedte van het uitvoervignet met één resolutie, de breedte van de eerste weergave van een uitvoervignet met meerdere resoluties, of &#39;0&#39; in het geval van een piramidevignet. Voor kabinetsstijlbestanden wordt de uitvoerresolutie gebruikt als achtervoegsel van het bestand. *[!DNL destFile]* wordt genegeerd wanneer  `-info` wordt opgegeven.
