---
description: Eigenschapgegevens worden geretourneerd als reactie op de volgende req=-typen imageprops en props.
seo-description: Eigenschapgegevens worden geretourneerd als reactie op de volgende req=-typen imageprops en props.
seo-title: Eigenschappen
solution: Experience Manager
title: Eigenschappen
topic: Scene7 Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Eigenschappen{#properties}

Eigenschapsgegevens worden geretourneerd als reactie op de volgende typen req=: imageprops en props.

De antwoordgegevens zijn opgemaakt om te kunnen worden gelezen als Java-eigenschappen. Een typisch antwoord op teksteigenschappen heeft deze algemene structuur:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` kan leeg zijn. Witruimte is optioneel aan het begin en einde van elke regel en voor en na het scheidingsteken &#39;=&#39;. Enkelvoudige of dubbele aanhalingstekens kunnen worden gebruikt om tekenreekswaarden in te sluiten, maar zijn niet vereist.

Tekenreekswaarden kunnen escape-tekens in de stijl JAVA bevatten, zoals \n, \t, \:. of \\.

**Zie ook**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
