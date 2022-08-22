---
title: Algemene gegevenstypen
description: Cataloguskenmerken en -velden kunnen gegevens van een van de volgende typen bevatten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Algemene gegevenstypen{#common-data-types}

Cataloguskenmerken en -velden kunnen gegevens van een van de volgende typen bevatten.

**Kleur**

Kleurwaarde. Hexadecimale, verpakte RGB-waarde, optioneel voorafgegaan door 0x. De waarde RGB bijvoorbeeld `128,255,0` kan worden opgegeven als `0x80ff00` of `80ff00`.

**Markering**

`0`=false, `1`=true, elke andere waarde betekent onbekend of niet opgegeven.

**Enum**

`0` Hiermee wordt een onbekende of niet-opgegeven waarde aangegeven, gelijk aan een leeg veld. Geldig `enum` waarden zijn opeenvolgende gehele getallen, te beginnen met 1.

**Geheel getal**

Waarde van geheel getal met teken (bijvoorbeeld `0, -12, 34`). `0` of negatieve waarden kunnen een speciale betekenis hebben.

**Reëel nummer**

Waarde van ondertekend zwevend punt (bijvoorbeeld `0, 12.5, 245 , -2.34e4`). 0 of negatieve waarden kunnen een speciale betekenis hebben.

**Tekstreeks**

Tekenreeksscheidingstekens zijn optioneel, tenzij de tekenreeks een `<CR>`, `<LF>`, of `<TAB>` tekens. Enkelvoudige en dubbele aanhalingstekens kunnen als scheidingstekens worden gebruikt. Wanneer aanhalingstekens worden gebruikt, moet een dergelijk aanhalingsteken dat in de tekenreeks is ingesloten, worden ontsnapt door twee opeenvolgende aanhalingstekens te gebruiken (bijvoorbeeld &#39; `This month''s Special`&quot;).
