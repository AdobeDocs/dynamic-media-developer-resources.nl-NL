---
title: Eigenschappen
description: Eigenschapgegevens worden geretourneerd als reactie op de volgende req=-typen imageprops en props.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Eigenschappen{#properties}

Eigenschapsgegevens worden geretourneerd als reactie op de volgende typen req=: imageprops en props.

De antwoordgegevens zijn opgemaakt om te kunnen worden gelezen als Java™-eigenschappen. Een typisch antwoord op teksteigenschappen heeft deze algemene structuur:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` Kan leeg zijn. Witruimte is optioneel aan het begin en einde van elke regel en voor en na het scheidingsteken &#39;=&#39;. Enkelvoudige of dubbele aanhalingstekens kunnen worden gebruikt om tekenreekswaarden in te sluiten, maar zijn niet vereist.

Tekenreekswaarden kunnen escape-tekens in de stijl JAVA bevatten, zoals `\n`, `\t`, `\:`, of `\\`.

**Zie ook**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
