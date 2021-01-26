---
description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req=img of req=tmb.
seo-description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req=img of req=tmb.
seo-title: Afbeeldingen
solution: Experience Manager
title: Afbeeldingen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Afbeeldingen{#images}

De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req=img of req=tmb.

Het MIME-type van de HTTP-respons wordt bepaald door `fmt=`, of als `fmt=` niet is opgegeven, is het `<image/jpeg>`.

De status van de HTTP-reactie is &#39;200 OK&#39; als de aanvraagmethode een onvoorwaardelijke `GET` of `HEAD` was.

De server kan reageren met status &#39;304&#39; (niet gewijzigd) en geen afbeeldingsgegevens retourneren als reactie op een voorwaardelijk `GET` verzoek (dat een geldige `If-Modified-Since` of `If-None-Match` header bevat).
