---
description: Directe toegang tot op paden gebaseerde elementen toestaan.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Directe toegang tot op paden gebaseerde elementen toestaan.

Wanneer dit kenmerk is gedefinieerd, is padgebaseerde toegang toegestaan of beperkt voor de opgegeven objecttypen, afhankelijk van of de `include` of `exclude` trefwoord wordt gebruikt.

>[!NOTE]
>
>Als de `AllowDirectAccess` kenmerk is niet opgegeven, de standaardwaarde is `exclude`.

* `include` verleent toegang voor de gespecificeerde objecten types en beperkt toegang voor alle anderen.
* `exclude` beperkt de toegang voor de opgegeven objecttypen en staat toegang voor alle andere objecten toe.

Als beide `include` noch `exclude` is gespecificeerd, `include` wordt aangenomen.

De volgende typen kunnen worden beheerd:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Voorbeelden {#section-4c3765ebaa4245a799b454fc196f9237}

* Alleen directe toegang toestaan voor `IS` en `STATIC` objecttypen

   `AllowDirectAccess=include:IS,STATIC`

* Directe toegang toestaan voor alle objecttypen behalve `IS` en `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Directe toegang toestaan voor *nee* objecttypen (geen opnemen)

   `AllowDirectAccess=include:`

* Directe toegang toestaan voor *alles* objecttypen (geen uitsluiten)

   `AllowDirectAccess=exclude:`

* Equivalent met `include:IS,STATIC` (if `include`/ `exclude` niet aanwezig is, `include` wordt aangenomen)

   `AllowDirectAccess=IS,STATIC`

   Dit is de standaardwaarde die wordt gebruikt als de `AllowDirectAccess` attribute is not specified for this company.

* Geen opnemen, gelijk aan `include:` (if `include`/ `exclude` niet aanwezig is, `include` wordt aangenomen)

   `AllowDirectAccess=`
