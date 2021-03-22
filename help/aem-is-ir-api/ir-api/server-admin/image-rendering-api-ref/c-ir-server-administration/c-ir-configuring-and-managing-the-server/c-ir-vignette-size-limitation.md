---
description: Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.
seo-description: Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.
seo-title: Limiet voor vignetgrootte
solution: Experience Manager
title: Limiet voor vignetgrootte
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,beheerder,praktijkgericht
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Limiet vignetgrootte{#vignette-size-limitation}

Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.

Wijzig de waarde van `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] als uw toepassing steun voor niet-piramide vignettes met een beeldgebied (breedte x hoogte) groter dan deze grens vereist.

>[!NOTE]
>
>`attribute::MaxPix` en  `IS::MaxMessageSize` kan ook moeten worden aangepast om ongewoon grote responsiegrootten mogelijk te maken. Raadpleeg de documentatie bij de beeldserver voor meer informatie.

