---
title: Limiet voor vignetgrootte
description: Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Limiet voor vignetgrootte{#vignette-size-limitation}

Bij het renderen van afbeeldingen wordt een formaatbeperking van twee megapixels toegepast voor niet-piramidevignetten.

Wijzig de waarde van `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] als uw toepassing ondersteuning vereist voor niet-piramidevignetten waarvan het afbeeldingsgebied (breedte x hoogte) groter is dan deze limiet.

>[!NOTE]
>
>De kenmerken aanpassen `attribute::MaxPix` en `IS::MaxMessageSize` om ongebruikelijk grote reactieafbeeldingsgrootten toe te staan. Raadpleeg de documentatie bij de beeldserver voor meer informatie.
