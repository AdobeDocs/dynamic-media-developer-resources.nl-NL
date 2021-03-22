---
description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden img heeft, zuivert
seo-description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden img heeft, zuivert
seo-title: Afbeeldingen
solution: Experience Manager
title: Afbeeldingen
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Afbeeldingen{#images}

De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden heeft: img, foutopsporing

Het MIME-type van de HTTP-respons wordt bepaald door `fmt=`, of als `fmt=` niet is opgegeven, is dit afhankelijk van de waarde van `attribute::Format`.

De status van de HTTP-reactie is &#39;200 OK&#39; als de aanvraagmethode een onvoorwaardelijke `GET` of `HEAD` was.

De server kan reageren met status &#39;304&#39; (niet gewijzigd) en geen afbeeldingsgegevens retourneren als reactie op een voorwaardelijk `GET` verzoek (met het veld [!DNL If-Modified-Since] aanwezig in `request-header`).
