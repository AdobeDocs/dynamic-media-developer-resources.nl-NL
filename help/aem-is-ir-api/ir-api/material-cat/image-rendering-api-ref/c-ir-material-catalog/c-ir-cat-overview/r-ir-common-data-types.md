---
description: Cataloguskenmerken en -velden kunnen gegevens van een van de volgende typen bevatten.
solution: Experience Manager
title: Algemene gegevenstypen
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Algemene gegevenstypen{#common-data-types}

Cataloguskenmerken en -velden kunnen gegevens van een van de volgende typen bevatten.

**Kleur**

Kleurwaarde. Hexadecimale, verpakte RGB-waarde, optioneel voorafgegaan door 0x. De RGB-waarde `128,255,0` kan bijvoorbeeld worden opgegeven als `0x80ff00` of `80ff00`.

**Markering**

`0`=false,  `1`=true, elke andere waarde betekent onbekend of niet opgegeven.

**Enum**

0 geeft een onbekende of niet-opgegeven waarde aan, gelijk aan een leeg veld. Geldige `enum` waarden zijn opeenvolgende gehele getallen, te beginnen met 1.

**Geheel getal**

Waarde van geheel getal met teken (bijvoorbeeld 0, -12, 34). 0 of negatieve waarden kunnen een speciale betekenis hebben.

**Reëel nummer**

Waarde van ondertekend zwevend punt (bijvoorbeeld `0, 12.5, 245 , -2.34e4`). 0 of negatieve waarden kunnen een speciale betekenis hebben.

**Tekstreeks**

Tekenreeksscheidingstekens zijn optioneel, tenzij de tekenreeks `<CR>`, `<LF>` of `<TAB>` tekens bevat. Enkelvoudige en dubbele aanhalingstekens kunnen als scheidingstekens worden gebruikt. Wanneer aanhalingstekens worden gebruikt, moet een dergelijk aanhalingsteken dat in de tekenreeks is ingesloten, worden omzeild door twee opeenvolgende aanhalingstekens te gebruiken (bijvoorbeeld &quot; `This month''s Special`&quot;).
