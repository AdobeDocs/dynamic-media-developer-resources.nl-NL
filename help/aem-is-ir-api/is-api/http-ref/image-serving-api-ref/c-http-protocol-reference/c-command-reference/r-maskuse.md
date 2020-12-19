---
description: Maskergebruik van afbeelding. Hiermee geeft u op hoe het masker of het alfakanaal van de afbeelding wordt gebruikt voor bewerkingen in de afbeelding (bijvoorbeeld colorize=). Wanneer het effect in een effectlaag wordt opgegeven, is het mogelijk het effect toe te passen op het achtergrondgebied van de bovenliggende laag of op de volledige bovenliggende laagrechthoek.
seo-description: Maskergebruik van afbeelding. Hiermee geeft u op hoe het masker of het alfakanaal van de afbeelding wordt gebruikt voor bewerkingen in de afbeelding (bijvoorbeeld colorize=). Wanneer het effect in een effectlaag wordt opgegeven, is het mogelijk het effect toe te passen op het achtergrondgebied van de bovenliggende laag of op de volledige bovenliggende laagrechthoek.
seo-title: maskUse
solution: Experience Manager
title: maskUse
topic: Scene7 Image Serving - Image Rendering API
uuid: 2c70da87-f869-495a-be50-226a4516e002
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# maskUse{#maskuse}

Maskergebruik van afbeelding. Hiermee geeft u op hoe het masker of het alfakanaal van de afbeelding wordt gebruikt voor bewerkingen in de afbeelding (bijvoorbeeld colorize=). Wanneer het effect in een effectlaag wordt opgegeven, is het mogelijk het effect toe te passen op het achtergrondgebied van de bovenliggende laag of op de volledige bovenliggende laagrechthoek.

`maskUse=norm|invert|off`

In de volgende tabel ziet u het effect van `maskUse=` afhankelijk van de beschikbaarheid en het type masker (alfakanaal) dat aan de laagafbeelding is gekoppeld.

<table id="table_B765F6A765F548948531AF26DA0B4360"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Waarde</b> </th> 
   <th class="entry"> <b> Geen masker</b> </th> 
   <th class="entry"> <b> Niet-gekoppelde alfa (of afzonderlijke maskerafbeelding)</b> </th> 
   <th class="entry"> <b> Gekoppelde (vooraf vermenigvuldigde) alfa</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> uit  </span> </p> </td> 
   <td> <p> Dekkende afbeeldingsrechthoek </p> </td> 
   <td> <p> Dekkende afbeeldingsrechthoek </p> </td> 
   <td> <p> Voorgrond van afbeelding boven rechthoek gevuld met effen zwart </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> norm  </span> </p> </td> 
   <td> <p> Dekkende afbeeldingsrechthoek </p> </td> 
   <td> <p> Voorgrond van afbeelding </p> </td> 
   <td> <p> Voorgrond van afbeelding of laag </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> omkeren  </span> </p> </td> 
   <td> <p> Verborgen laag </p> </td> 
   <td> <p> Achtergrondgebied van afbeelding </p> </td> 
   <td> <p> Achtergrondgebied van afbeelding of laag gevuld met effen zwart </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-f36ad1af348e45aeb3eb336544df30b0}

Kenmerk afbeelding of laag. Is op laag 0 van toepassing als `layer=comp`. Als deze optie is opgegeven in een effectlaag, wijzigt de opdracht het masker dat is overgenomen van de bovenliggende laag.

Het gedrag van `maskUse=` is ongedefinieerd en wordt niet ondersteund wanneer dit wordt opgegeven met tekst of effen kleurlagen wanneer er geen afbeeldingsmasker van toepassing is (opgegeven met `mask=` of `catalog::Mask`).

## Standaard {#section-982dd8174641437786dcb3729ace6428}

`maskUse=norm`

## Voorbeeld {#section-daa371e9be5547368ff6772342acba0a}

Vullen met kleur op de achtergrond van een afbeelding; de voorgrond van de afbeelding wordt gedefinieerd door een aparte maskerafbeelding. Dit wordt bereikt door de achtergrond van de gekleurde afbeelding bovenaan in lagen te plaatsen als de ongewijzigde afbeelding:

`http://server/myRootId/myImageId?layer=1&src=myImageId&mask=myImgMask&maskUse=invert&colorize=0x306090`

## Zie ook {#section-f239d8f4ce70434f8d30e482ed60ee5e}

[color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)
