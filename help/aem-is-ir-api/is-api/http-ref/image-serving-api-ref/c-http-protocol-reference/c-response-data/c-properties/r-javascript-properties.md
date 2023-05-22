---
description: Als JavaScript™ is opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om te worden geparseerd als een include-bestand voor JavaScript™.
solution: Experience Manager
title: JavaScript™-eigenschappen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# JavaScript™-eigenschappen{#javascript-properties}

Als JavaScript™ is opgegeven als de indeling voor reacties, worden de antwoordgegevens opgemaakt om te worden geparseerd als een include-bestand voor JavaScript™.

Een typisch JavaScript™-eigenschapsantwoord heeft de volgende algemene structuur:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* kan leeg zijn. Witruimte is optioneel aan het begin en einde van elke regel en voor en na het scheidingsteken =. Alle waarden worden ingesloten door enkele aanhalingstekens. Enkele aanhalingstekens in tekenreeksen worden met twee opeenvolgende enkele aanhalingstekens genegeerd.

Als u een reactie van een JavaScript™-eigenschap wilt parseren, moeten alle objecten waarnaar in het antwoord wordt verwezen, worden gemaakt voordat het eigenschappenbestand wordt geladen. Hieronder ziet u een voorbeeld voor het gebruik van `req=props` om de grootte van de reactieafbeelding in JavaScript™ te verkrijgen:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
