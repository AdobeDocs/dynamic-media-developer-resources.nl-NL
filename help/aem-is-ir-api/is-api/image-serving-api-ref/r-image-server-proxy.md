---
description: Een proxy van een afbeeldingsserver kan worden gebruikt om het formaat van afbeeldingen voor Japanse telefoons te wijzigen.
seo-description: Een proxy van een afbeeldingsserver kan worden gebruikt om het formaat van afbeeldingen voor Japanse telefoons te wijzigen.
seo-title: Proxy afbeeldingsserver
solution: Experience Manager
title: Proxy afbeeldingsserver
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Proxy voor afbeeldingsserver{#image-server-proxy}

Een proxy van een afbeeldingsserver kan worden gebruikt om het formaat van afbeeldingen voor Japanse telefoons te wijzigen.

## URL-indeling {#section-2e8c40b0547c4f99874cdf502b338940}

Het url formaat voor de volmacht IS is zeer gelijkaardig aan regelmatige verzoeken van IS. Om het even welk IS die bepalingen tot de volmacht worden overgegaan wordt overgegaan door aan de Server van het Beeld. U kunt informatie over de modifiers van IS in [de Verwijzing van het Protocol van HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e) vinden.

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Proxy-specifieke wijziginglijst {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Hiermee geeft u het percentage op van de bruikbare breedte van het apparaat dat u als afbeeldingsbreedte wilt gebruiken. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Hiermee geeft u het percentage op van de bruikbare hoogte van het apparaat dat u als afbeeldingshoogte wilt gebruiken. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Hiermee wordt het percentage opgegeven van de eigenschap Memory Limit Embedded Media van het apparaat om de responsgrootte te beperken tot. Dit geldt alleen voor JPG-reacties. De kwaliteit van de afbeelding wordt verlaagd totdat de responsgrootte binnen het opgegeven percentage valt. </p></td> 
 </tr> 
</table>

## Limiet voor ingesloten afbeeldingsgeheugen {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Als het apparaat een beperking heeft op de grootte van afbeeldingen die op een webpagina kunnen worden ingesloten, is de afbeeldingsgrootte beperkt tot die grootte zolang de responsindeling JPG is. De proxy beperkt de reacties tot 500 MB als het apparaat geen limiet heeft.

## Achtergrondverwerking {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

De proxy downloadt, verifieert en laadt het bestand met apparaatatlas eenmaal per dag. De controle trekt verschillende eigenschappen voor verschillende apparaten uit en vergelijkt hen met verwachte waarden alvorens de nieuwe gegevens goed te keuren.
