---
description: Directe toegang tot op paden gebaseerde elementen toestaan.
seo-description: Directe toegang tot op paden gebaseerde elementen toestaan.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Directe toegang tot op paden gebaseerde elementen toestaan.

Wanneer dit kenmerk wordt gedefinieerd, is padgebaseerde toegang toegestaan of beperkt voor de opgegeven objecttypen, afhankelijk van het feit of het trefwoord `include` of `exclude` wordt gebruikt.

>[!NOTE]
>
>Als het `AllowDirectAccess` attribuut niet wordt gespecificeerd, is de standaardwaarde `exclude`.

* `include` verleent toegang voor de gespecificeerde objecten types en beperkt toegang voor alle anderen.
* `exclude` beperkt de toegang voor de opgegeven objecttypen en staat toegang voor alle andere objecten toe.

Als noch `include` noch `exclude` wordt gespecificeerd, `include` wordt verondersteld.

De volgende typen kunnen worden beheerd:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Voorbeelden {#section-4c3765ebaa4245a799b454fc196f9237}

* Alleen directe toegang toestaan voor objecttypen `IS` en `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Directe toegang toestaan voor alle objecttypen behalve `IS` en `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Directe toegang toestaan voor objecttypen *no* (d.w.z. geen opnemen)

   `AllowDirectAccess=include:`

* Directe toegang toestaan voor *alle objecttypen* (d.w.z. geen uitsluiten)

   `AllowDirectAccess=exclude:`

* Gelijk aan `include:IS,STATIC` (als `include`/ `exclude` niet aanwezig is, wordt `include` verondersteld)

   `AllowDirectAccess=IS,STATIC`

   Merk op dat de standaardwaarde is die wordt gebruikt als het `AllowDirectAccess` attribuut niet voor dit bedrijf wordt gespecificeerd.

* Geen opnemen, gelijk aan `include:` (als `include`/ `exclude` niet aanwezig is, wordt `include` aangenomen)

   `AllowDirectAccess=`

