---
description: Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.
solution: Experience Manager
title: Eigenschappen van Text (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Eigenschappen van Text (Java){#text-java-properties}

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

Tekenreekswaarden kunnen escape-tekens in de stijl JAVA bevatten, zoals `\n`, `\t`, `\:`, of `\\`.
