---
description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden img heeft, zuivert.
solution: Experience Manager
title: Afbeeldingen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Afbeeldingen{#images}

De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden heeft: img, foutopsporing

Het MIME-type van de HTTP-respons wordt bepaald door `fmt=`, of als `fmt=` niet is opgegeven, is dit afhankelijk van de waarde van `attribute::Format`.

De status van de HTTP-reactie is &#39;200 OK&#39; als de aanvraagmethode een onvoorwaardelijke `GET` of `HEAD` was.

De server kan reageren met status &#39;304&#39; (niet gewijzigd) en geen afbeeldingsgegevens retourneren als reactie op een voorwaardelijk `GET` verzoek (met het veld [!DNL If-Modified-Since] aanwezig in `request-header`).
