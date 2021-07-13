---
description: Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.
solution: Experience Manager
title: Limiet voor vignetgrootte
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Limiet voor vignetgrootte{#vignette-size-limitation}

Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.

Wijzig de waarde van `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] als uw toepassing steun voor niet-piramide vignettes met een beeldgebied (breedte x hoogte) groter dan deze grens vereist.

>[!NOTE]
>
>`attribute::MaxPix` en  `IS::MaxMessageSize` kan ook moeten worden aangepast om ongewoon grote responsiegrootten mogelijk te maken. Raadpleeg de documentatie bij de beeldserver voor meer informatie.
