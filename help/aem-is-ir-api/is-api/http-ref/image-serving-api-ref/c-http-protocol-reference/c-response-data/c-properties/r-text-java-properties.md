---
description: Als tekst wordt opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om leesbaar te zijn als Java-eigenschappen.
solution: Experience Manager
title: Eigenschappen van Text (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
