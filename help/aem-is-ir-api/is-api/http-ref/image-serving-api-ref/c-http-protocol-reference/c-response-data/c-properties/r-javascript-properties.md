---
description: Als javascript als reactieformaat wordt gespecificeerd, zijn de antwoordgegevens geformatteerd om als JavaScript worden geparseerd omvat dossier.
seo-description: Als javascript als reactieformaat wordt gespecificeerd, zijn de antwoordgegevens geformatteerd om als JavaScript worden geparseerd omvat dossier.
seo-title: JavaScript-eigenschappen
solution: Experience Manager
title: JavaScript-eigenschappen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# JavaScript-eigenschappen{#javascript-properties}

Als javascript als reactieformaat wordt gespecificeerd, zijn de antwoordgegevens geformatteerd om als JavaScript worden geparseerd omvat dossier.

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

*`propertyValue`* mag leeg zijn. Witruimte is optioneel aan het begin en einde van elke regel en voor en na het scheidingsteken =. Alle waarden worden ingesloten door enkele aanhalingstekens. Enkele aanhalingstekens in tekenreeksen worden met twee opeenvolgende enkele aanhalingstekens genegeerd.

Als u een reactie met JavaScript-eigenschappen wilt parseren, moet(en) waarnaar in het antwoord wordt verwezen, worden gemaakt voordat het eigenschappenbestand wordt geladen. Hier volgt een voorbeeld voor het gebruik van `req=props` om de grootte van de reactieafbeelding in JavaScript te verkrijgen:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

