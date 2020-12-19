---
description: Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.
seo-description: Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.
seo-title: Limiet voor vignetgrootte
solution: Experience Manager
title: Limiet voor vignetgrootte
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Limiet vignetgrootte{#vignette-size-limitation}

Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.

Wijzig de waarde van `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] als uw toepassing steun voor niet-piramide vignettes met een beeldgebied (breedte x hoogte) groter dan deze grens vereist.

>[!NOTE]
>
>`attribute::MaxPix` en  `IS::MaxMessageSize` kan ook moeten worden aangepast om ongewoon grote responsiegrootten mogelijk te maken. Raadpleeg de documentatie bij de beeldserver voor meer informatie.

