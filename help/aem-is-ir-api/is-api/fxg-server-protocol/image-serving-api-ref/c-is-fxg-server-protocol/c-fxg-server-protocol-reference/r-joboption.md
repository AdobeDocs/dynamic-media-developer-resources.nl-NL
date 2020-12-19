---
description: PDF-taakopties toepassen. Een bestand met taakopties of een PDF-voorinstelling is een bestand dat door Illustrator is gegenereerd in het dialoogvenster Opslaan als PDF-opties of in het dialoogvenster PDF-voorinstellingen in InDesign.
seo-description: PDF-taakopties toepassen. Een bestand met taakopties of een PDF-voorinstelling is een bestand dat door Illustrator is gegenereerd in het dialoogvenster Opslaan als PDF-opties of in het dialoogvenster PDF-voorinstellingen in InDesign.
seo-title: joboption
solution: Experience Manager
title: joboption
topic: Scene7 Image Serving - Image Rendering API
uuid: 7288cf29-850f-4121-8425-5f995daac22d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# joboption{#joboption}

PDF-taakopties toepassen. Een bestand met taakopties of een PDF-voorinstelling is een bestand dat door Illustrator is gegenereerd in het dialoogvenster Opslaan als PDF-opties of in het dialoogvenster PDF-voorinstellingen in InDesign.

` joboption= *`value`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span></span> </p> </td> 
  <td class="stentry"> <p>De IPSID van het bestand met taakopties. </p></td> 
 </tr> 
</table>

Het dossier van baanopties kan door IPS/SPS worden geupload en worden gepubliceerd. De PDF-opties in het bestand met taakopties worden gebruikt wanneer de PDF wordt gegenereerd.

De volgende opties worden momenteel ondersteund:

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Algemeen </p></td> 
  <td class="stentry"> <p> Compatibiliteit </p> <p> Compressie op objectniveau </p> <p> Miniaturen insluiten </p> <p> Optimaliseren voor snelle webweergave </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Afbeeldingen </p></td> 
  <td class="stentry"> <p> Downsampling, Resolutie, Drempel en Compressie voor kleur, grijs en mono </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Lettertypen </p></td> 
  <td class="stentry"> <p> Alle fonts insluiten </p> <p> OpenType-lettertypen insluiten </p> <p> Subset maken van ingesloten lettertypen wanneer percentage gebruikte tekens kleiner is dan: </p> <p> Altijd lijst insluiten </p> <p> Nooit invoegen </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Kleur </p></td> 
  <td class="stentry"> <p> Kleurstrategie (alleen labelen van afbeeldingen wordt behandeld als alles labelen) </p> <p> Render-intentie document </p> <p> Alleen de volgende werkruimten worden ondersteund voor 4.2.5. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB met coderingsbereik [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> Platte XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">Lineaire ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8-bits </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8-bits </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">Grijs <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Grijsgamma 1,8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Grijsgamma 2,2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Puntverbreding 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Puntverbreding 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Puntverbreding 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Puntverbreding 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Puntverbreding 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> CMYK-waarden behouden voor gekalibreerde CMYK-kleurruimten </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Geavanceerd </p></td> 
  <td class="stentry"> <p>OPI-opmerkingen behouden is altijd ingeschakeld. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Normen </p></td> 
  <td class="stentry"> <p>Compatibiliteitsnorm. </p></td> 
 </tr> 
</table>

