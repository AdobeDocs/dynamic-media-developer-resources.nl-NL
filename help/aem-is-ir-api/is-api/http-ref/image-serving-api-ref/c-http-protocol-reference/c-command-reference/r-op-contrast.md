---
description: Pas het contrast aan. Hiermee past u het afbeeldingscontrast aan door de helderheid van pixels met meer dan 50% helderheid te verhogen en de helderheid van pixels met minder dan 50% helderheid te verminderen.
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# op_contrast{#op-contrast}

Pas het contrast aan. Hiermee past u het afbeeldingscontrast aan door de helderheid van pixels met meer dan 50% helderheid te verhogen en de helderheid van pixels met minder dan 50% helderheid te verminderen.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Contrastaanpassing in procenten (-100...100 int). </p></td> 
 </tr> 
</table>

## Eigenschappen {#section-d319ed55057344eab0a3c93f720acdbf}

Laag, opdracht. Is van toepassing op de huidige laag of op de samengestelde afbeelding als `layer=comp`. Genegeerd door effectlagen.

## Standaard {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, voor geen wijziging in het contrast. CMYK-afbeeldingen of -lagen worden omgezet in RGB voordat de bewerking wordt toegepast.

## Voorbeeld {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Verlaag het contrast en de scherpte van een afbeeldingslaag van hogere kwaliteit, zodat deze visueel overeenkomt met een achtergrondfoto van lage kwaliteit:

… `&op_blur=3&op_contrast=-12&`

Bij een toekomstige release wordt mogelijk de mediaanhelderheid van de afbeelding gebruikt in plaats van een vaste helderheid van 50%.
