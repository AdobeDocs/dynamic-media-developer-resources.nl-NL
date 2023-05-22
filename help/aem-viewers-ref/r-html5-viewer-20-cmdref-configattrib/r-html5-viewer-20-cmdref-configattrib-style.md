---
title: stijl
description: stijl
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# stijl{#style}

U kunt het volgende bevel zowel van het URL vraagkoord als config toepassen. Het bevel dat in het URL vraagkoord wordt toegepast neemt altijd belangrijkheid over het zelfde bevel huidig in config.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Relatieve of absolute CSS-locatie. </p> <p>Hiermee geeft u de locatie van het aangepaste CSS-bestand op. Als de <span class="codeph"><span class="varname"> cssPath</span></span> is relatief, wordt deze omgezet op basis van de locatie van de HTML-pagina van de viewer en de waarde van <span class="codeph"> contentUrl=</span> parameter. </p> </td> 
  </tr> 
 </tbody> 
</table>

Alle elementverwijzingen in het CSS-bestand worden omgezet op de locatie van het CSS-bestand, niet op de locatie van de aanroepende HTML-pagina.

## Eigenschappen {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Optioneel.

## Standaard {#section-79a827f7a3bb4f36b3d72c309155059e}

Geen.

## Voorbeelden {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
