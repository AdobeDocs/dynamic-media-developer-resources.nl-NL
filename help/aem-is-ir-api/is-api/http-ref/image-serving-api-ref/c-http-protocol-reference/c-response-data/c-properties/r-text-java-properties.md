---
description: Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.
seo-description: Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.
seo-title: Eigenschappen van Text (Java)
solution: Experience Manager
title: Eigenschappen van Text (Java)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Teksteigenschappen (Java){#text-java-properties}

Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.

Een typisch antwoord op teksteigenschappen heeft deze algemene structuur:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* mag leeg zijn. Witruimte is optioneel aan het begin en einde van elke regel en voor en na het scheidingsteken =. Enkelvoudige of dubbele aanhalingstekens kunnen worden gebruikt om tekenreekswaarden in te sluiten, maar zijn niet vereist.

Tekenreekswaarden kunnen escape-tekens in de stijl JAVA bevatten, zoals `\n`, `\t`, `\:` of `\\`.
