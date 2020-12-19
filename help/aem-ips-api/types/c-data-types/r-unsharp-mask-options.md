---
description: Instellingen die de scherpte van afbeeldingen voor geoptimaliseerde TIF-piramidebestanden helpen verbeteren.
seo-description: Instellingen die de scherpte van afbeeldingen voor geoptimaliseerde TIF-piramidebestanden helpen verbeteren.
seo-title: UnsharpMaskOptions
solution: Experience Manager
title: UnsharpMaskOptions
topic: Scene7 Image Production System API
uuid: 73073de0-41b6-471c-8887-f6b94ed2af90
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# UnsharpMaskOptions{#unsharpmaskoptions}

Instellingen die de scherpte van afbeeldingen voor geoptimaliseerde TIF-piramidebestanden helpen verbeteren.

`unsharpMaskOptions=[ *`hoeveelheid, straal, drempel, monochroom`*]`

## Parameters {#section-c3f0d03136ba4422819cb463bd393885}

Geef een waarde op voor `unsharpMaskOptions`-opties met `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Naam </th>
   <th colname="col2" class="entry"> Type </th>
   <th colname="col3" class="entry"> Beschrijving </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> bedrag</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:dubbel</span></td>
   <td colname="col3"><p>Hiermee bepaalt u het contrast dat wordt toegepast op randpixels. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Bereik: 0,0 - 5,0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Standaard: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> radius</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:dubbel</span></td>
   <td colname="col3"><p>Hiermee regelt u de scherpte door het aantal pixels rond de rand van een afbeelding in te stellen. De juiste waarde is afhankelijk van de grootte van de afbeelding. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Bereik: 0,0 - 250,0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Bij lage waarden worden alleen de randpixels verscherpt. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Bij hoge waarden wordt een grotere reeks pixels verscherpt. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> drempel</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Hiermee bepaalt u hoe verschillende pixels moeten zijn afkomstig uit het omringende gebied voordat deze worden beschouwd als randpixels en kunnen worden verscherpt. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Bereik: 0 - 255 (alleen gehele getallen). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Standaard: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monochroom</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Waarden zijn alleen <span class="codeph"> 0</span> of <span class="codeph"> 1</span>. </p><p>Stel in op <span class="codeph"> 0</span> om toe te passen op elke kleurcomponent afzonderlijk of op <span class="codeph"> 1</span> om alleen toe te passen op helderheid (intensiteit) van afbeelding. Het laagmasker of het samengestelde masker wordt ook verscherpt. </p><p><span class="codeph"><span class="varname"> </span></span> monochrome afbeeldingen worden genegeerd. </p></td>
  </tr>
 </tbody>
</table>

## Voorbeeld {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Wordt gebruikt door {#section-db8124a5468b498694a780f8a56a4560}

Het type `unsharpMaskOptions` wordt gebruikt door:

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Referentie voor API voor afbeeldingsservice: op_usm](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)

