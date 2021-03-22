---
description: Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.
seo-description: Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.
seo-title: Eigenschappen van Text (Java)
solution: Experience Manager
title: Eigenschappen van Text (Java)
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
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
