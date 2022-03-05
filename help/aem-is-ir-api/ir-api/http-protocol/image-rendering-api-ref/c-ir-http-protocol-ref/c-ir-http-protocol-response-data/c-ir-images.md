---
title: Afbeeldingen
description: De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden img heeft, zuivert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Afbeeldingen{#images}

De gegevens van het beeld zijn teruggekeerd als een verzoek met succes voltooit, en als het verzoek of geen req= bevel omvat, of als req= één van de volgende waarden heeft: img, foutopsporing

Het MIME-type van de HTTP-respons wordt bepaald door `fmt=`of, indien `fmt=` is niet opgegeven, hangt af van de waarde van `attribute::Format`.

De status van de HTTP-reactie is &#39;200 OK&#39; als de aanvraagmethode onvoorwaardelijk was `GET` of `HEAD`.

De server kan reageren met status &#39;304&#39; (niet gewijzigd) en geen afbeeldingsgegevens retourneren als reactie op een voorwaardelijke `GET` verzoek (met de [!DNL If-Modified-Since] in het `request-header`).
