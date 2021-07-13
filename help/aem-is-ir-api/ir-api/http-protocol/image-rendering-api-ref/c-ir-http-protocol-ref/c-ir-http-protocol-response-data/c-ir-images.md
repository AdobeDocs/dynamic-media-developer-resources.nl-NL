---
description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden img heeft, zuivert.
solution: Experience Manager
title: Afbeeldingen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Afbeeldingen{#images}

De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden heeft: img, foutopsporing

Het MIME-type van de HTTP-respons wordt bepaald door `fmt=`, of als `fmt=` niet is opgegeven, is dit afhankelijk van de waarde van `attribute::Format`.

De status van de HTTP-reactie is &#39;200 OK&#39; als de aanvraagmethode een onvoorwaardelijke `GET` of `HEAD` was.

De server kan reageren met status &#39;304&#39; (niet gewijzigd) en geen afbeeldingsgegevens retourneren als reactie op een voorwaardelijk `GET` verzoek (met het veld [!DNL If-Modified-Since] aanwezig in `request-header`).
