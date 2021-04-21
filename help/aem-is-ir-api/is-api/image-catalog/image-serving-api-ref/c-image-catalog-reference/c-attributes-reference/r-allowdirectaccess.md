---
description: Directe toegang tot op paden gebaseerde elementen toestaan.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
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

