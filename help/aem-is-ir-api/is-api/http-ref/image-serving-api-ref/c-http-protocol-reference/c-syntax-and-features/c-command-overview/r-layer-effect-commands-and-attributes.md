---
description: Met deze opdrachten kunt u laageffecten definiëren, zoals slagschaduw- of gloedeffecten. Effectlagen negeren alle andere opdrachten.
seo-description: Met deze opdrachten kunt u laageffecten definiëren, zoals slagschaduw- of gloedeffecten. Effectlagen negeren alle andere opdrachten.
seo-title: Laageffecten, opdrachten
solution: Experience Manager
title: Laageffecten, opdrachten
topic: Scene7 Image Serving - Image Rendering API
uuid: 5fef90d1-0507-497b-9187-869672996852
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Laageffecten{#layer-effect-commands}

Met deze opdrachten kunt u laageffecten definiëren, zoals slagschaduw- of gloedeffecten. Effectlagen negeren alle andere opdrachten.

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p></td> 
  <td class="stentry"> <p>Hiermee geeft u de overvloeimodus voor lagen op. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> kleur</a> </p></td> 
  <td class="stentry"> <p>Hiermee geeft u de hoofdkleur en dekking van het effect op. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> effect</a> </p></td> 
  <td class="stentry"> <p>Hiermee start u het segment van de effectlaag en geeft u de z-volgorde op. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>Hiermee geeft u op hoe het laagmasker (alfakanaal) van het bovenliggende element moet worden gebruikt. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_vervagen</a> </p></td> 
  <td class="stentry"> <p>Het effect wordt verzacht. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_kweken</a> </p></td> 
  <td class="stentry"> <p>Hiermee vergroot of verkleint u het laageffect. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_ruis</a> </p></td> 
  <td class="stentry"> <p>Hiermee voegt u ruis toe aan het effect. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>Hiermee verlaagt u de laagdekking. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>Plaatst de effectlaag ten opzichte van de bovenliggende laag. </p></td> 
 </tr> 
</table>
