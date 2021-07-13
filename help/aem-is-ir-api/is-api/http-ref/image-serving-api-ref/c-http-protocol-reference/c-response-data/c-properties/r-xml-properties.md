---
description: Als xml wordt opgegeven als de responsindeling, worden de antwoordgegevens opgemaakt als een XML-document dat door elke standaard XML-parser kan worden geparseerd.
solution: Experience Manager
title: XML-eigenschappen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
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
