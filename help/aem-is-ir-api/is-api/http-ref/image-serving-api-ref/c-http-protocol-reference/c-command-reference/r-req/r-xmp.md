---
description: XMP metagegevens. Retourneert de XMP metagegevens die zijn gekoppeld aan de afbeelding die is opgegeven in het aanvraagpad.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# xmp{#xmp}

XMP metagegevens. Retourneert de XMP metagegevens die zijn gekoppeld aan de afbeelding die is opgegeven in het aanvraagpad.

`req=xmp`

Andere opdrachten worden genegeerd. UTF-8-codering is van toepassing. De reactie is geformatteerd als XML met type MIME `text/xml`.

De HTTP-respons is cacheable met de TTL op basis van `catalog::Expiration`.

## Eigenschappen {#section-0d26b6a56c844153ae5cea4880370d00}

Request-kenmerk. Ongeacht de huidige laaginstelling.

## Standaard {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Als de URL geen afbeeldingspad of wijzigingstoetsen bevat, geldt het volgende:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Anders, `req=img`

## Voorbeelden {#section-34213692deab4a0f9037d5844132ee14}

Query uitvoeren op eigenschappen van afbeeldingsbestanden.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Cataloguseigenschappen voor query-afbeeldingen:

` http:// *`server`*/myRootId?req=catalogprops`

Open de eigenschappen van een item in een afbeeldingscatalogus vanuit JavaScript op de client die is ingesloten in een HTML-bestand:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Haal de maskerafbeelding voor een bepaald catalogusitem op, geschaald naar 25% van de oorspronkelijke grootte:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Een afbeelding aanvragen met een achtste formaat:

` http:// *`server`*/myRootId/myImageId?scl=8`

Dit is hetzelfde als:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

U kunt een miniatuur van een afbeelding aanvragen op basis van de miniatuurkenmerken die zijn opgegeven in de afbeeldingscatalogus:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Verzend een tekstbericht naar de serverlogboeken:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Zie ook {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [catalogus::doelen](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalogus::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md), [Miniatuurschaal](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f), [Eigenschappen](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), [Afbeeldingen met hyperlinks](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
