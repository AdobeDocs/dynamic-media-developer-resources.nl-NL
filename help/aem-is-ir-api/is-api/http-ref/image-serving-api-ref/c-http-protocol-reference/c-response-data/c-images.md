---
description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req=img of req=tmb.
seo-description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req=img of req=tmb.
seo-title: Afbeeldingen
solution: Experience Manager
title: Afbeeldingen
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Afbeeldingen{#images}

De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req=img of req=tmb.

Het MIME-type van de HTTP-respons wordt bepaald door `fmt=`, of als `fmt=` dit niet is opgegeven, wordt het bepaald `<image/jpeg>`.

De HTTP-antwoordstatus is &#39;200 OK&#39; als de aanvraagmethode onvoorwaardelijk `GET` of `HEAD`.

De server kan reageren met status &#39;304&#39; (niet gewijzigd) en geen afbeeldingsgegevens retourneren als reactie op een voorwaardelijk `GET` verzoek (dat een geldige `If-Modified-Since` of `If-None-Match` koptekst bevat).
