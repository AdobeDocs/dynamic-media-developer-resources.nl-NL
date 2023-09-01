---
title: JavaScript-eigenschappen
description: Als JavaScript is opgegeven als de indeling voor reacties, worden de antwoordgegevens zodanig opgemaakt dat deze worden geparseerd als een JavaScript-transactie; include-bestand.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# JavaScript-eigenschappen{#javascript-properties}

Als JavaScript is opgegeven als de indeling voor reacties, worden de antwoordgegevens zodanig opgemaakt dat deze worden geparseerd als een JavaScript-include-bestand.

Een typisch JavaScript-eigenschapsantwoord heeft de volgende algemene structuur:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

De *`propertyValue`* kan leeg zijn. Witruimte is optioneel aan het begin en einde van elke regel en voor en na het scheidingsteken =. Alle waarden staan tussen enkele aanhalingstekens. Enkele aanhalingstekens in tekenreeksen worden met twee opeenvolgende enkele aanhalingstekens genegeerd.

Als u een reactie met JavaScript-eigenschappen wilt parseren, moet een of meer objecten waarnaar in het antwoord wordt verwezen, worden gemaakt voordat het eigenschappenbestand wordt geladen. Hieronder ziet u een voorbeeld voor gebruik `req=props` om de grootte van de reactieafbeelding in JavaScript te verkrijgen:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
