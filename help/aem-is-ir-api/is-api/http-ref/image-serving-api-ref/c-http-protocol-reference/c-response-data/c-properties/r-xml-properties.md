---
description: Als xml wordt opgegeven als de responsindeling, worden de antwoordgegevens opgemaakt als een XML-document dat door elke standaard XML-parser kan worden geparseerd.
seo-description: Als xml wordt opgegeven als de responsindeling, worden de antwoordgegevens opgemaakt als een XML-document dat door elke standaard XML-parser kan worden geparseerd.
seo-title: XML-eigenschappen
solution: Experience Manager
title: XML-eigenschappen
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# XML-eigenschappen{#xml-properties}

Als xml wordt opgegeven als de responsindeling, worden de antwoordgegevens opgemaakt als een XML-document dat door elke standaard XML-parser kan worden geparseerd.

Een kenmerkend reactiedocument met eigenschappen heeft deze algemene structuur:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

Het element `<prop-group>` wordt gebruikt als buitenste container, en voor het groeperen van eigenschappen. Als een groep een naam heeft, komt de naam overeen met de naam van het Java/JavaScript-object.

>[!NOTE]
>
>Tekencodering kan worden opgegeven voor sommige typen `req=`. Zie de beschrijving van de specifieke `req=`opdracht voor meer informatie.

