---
title: perspectief
description: Perspectieftransformatie. Pas een perspectieftransformatie toe op de bronafbeelding van de laag om het gebied te vullen dat met de vierhoek is opgegeven. Andere gebieden van de laag blijven transparant.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# perspectief{#perspective}

Perspectieftransformatie. Pas een perspectieftransformatie toe op de bronafbeelding van de laag om het gebied te vullen dat met de vierhoek is opgegeven. Andere gebieden van de laag blijven transparant.

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>Perspectiefvierhoekige pixelcoördinaten (8 reële waarden, gescheiden door komma's). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>Genormaliseerde perspectiefvierhoekige coördinaten (8 realen, gescheiden door komma's). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>Opties voor het berekenen van nieuwe pixels (zie hieronder). </p></td> 
 </tr> 
</table>

*`perspQuad`* bestaat uit vier pixelcoördinaatwaarden in de samengestelde (of laag 0) coördinaatruimte, die in de linkerbovenhoek van de samengestelde afbeelding ontstaat.

`perspQuadN` bestaat uit vier genormaliseerde coördinaatwaarden, waarbij `0.0,0.0` komt overeen met de linkerbovenhoek van de samengestelde afbeelding/laag 0 en `1.0,1.0` in de rechterbenedenhoek.

De invoerafbeelding wordt zodanig getransformeerd dat de linkerbovenhoek van de invoerafbeelding wordt toegewezen aan de eerste coördinaatwaarde van `perspQuad[N]`, de rechterbovenhoek naar de tweede coördinaat, de rechterbenedenhoek naar de derde coördinaat en de linkerbenedenhoek naar de vierde coördinaat.

>[!NOTE]
>
>`pos=` kan worden gebruikt om de getransformeerde laag verder in de samengestelde afbeelding te plaatsen.

De perspectiefvierhoekige coördinaten kunnen zich buiten de samengestelde afbeelding bevinden.

Het gedrag is ongedefinieerd als de vierhoek niet geschikt is voor een perspectieftransformatie (bijvoorbeeld als twee of meer hoekpunten samenvallen, als drie of alle hoekpunten zich op dezelfde lijn bevinden, of als de vierhoek zichzelf doorsnijdt of concave is).

## Kwaliteitsoverwegingen {#section-7cc9056afa614300a9b8844d39739fc3}

Hoewel de standaardimplementatie een redelijk compromis tussen kwaliteit en prestaties oplevert, kan het soms nodig zijn om de resolutie van de bronafbeelding te verhogen om de scherpte te verbeteren of om deze te verminderen om aliasing-artefacten te verminderen.

Als de bron een afbeelding is, gebruikt u `scale=` een andere resolutie kiezen (ten opzichte van de volledige resolutie van de afbeelding). De opgegeven `scale=` De waarde wordt afgerond naar het volgende hogere PTIF resolutieniveau. In het geval van een geneste aanvraagbron kan de grootte van de afbeelding die door het geneste verzoek wordt geproduceerd, worden aangepast om de gewenste scherpte te verkrijgen. Voor tekstlagen wordt de resolutie van de invoerafbeelding (de gerenderde tekst) aangepast door een grotere size= waarde te selecteren in combinatie met een hogere resolutie die is opgegeven met `textAttr=`.

*`resOptions`* Hiermee kunt u een ander algoritme voor het berekenen van nieuwe pixels selecteren. De volgende waarden worden ondersteund (hoofdlettergevoelig):

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Waarde</b> </th> 
   <th class="entry"> <b> Beschrijving</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> Naaste buur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> Bidirectioneel. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> Standaard supersampling (standaard). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> Super sampling met verstelbare jitter (<span class="varname"> n</span> moet een geheel getal zijn tussen 0 en 200). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-818e57df0a1b4449888543bc6af77751}

Laag, opdracht. Is van toepassing op de huidige laag of op laag 0 als `layer=comp`. Genegeerd door effectlagen.

`res=` wordt altijd genegeerd wanneer perspectief zich op dezelfde laag bevindt. `size=` wordt genegeerd wanneer opgegeven voor afbeeldingslagen. `size=` en `res=` in lagen met `perspective=` zijn gereserveerd voor toekomstig gebruik.

## Standaard {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`voor geen perspectieftransformatie.

## Zie ook {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) , [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065), [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
