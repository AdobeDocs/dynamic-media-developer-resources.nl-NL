---
description: Parameter die alle viewers gemeen hebben.
seo-description: Parameter die alle viewers gemeen hebben.
seo-title: bijschrift
solution: Experience Manager
title: bijschrift
topic: Dynamic media
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bijschrift{#caption}

Parameter die alle viewers gemeen hebben.

>[!NOTE]
>
>Deze opdracht is niet van toepassing op Video Image Viewer.

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> bestand </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt een URL of pad naar de WebVTT-bijschriftinhoud opgegeven. De Beeldserver dient het WebVTT-bestand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u de standaardondertitelingsstatus op. Ingeschakeld is <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deze viewer ondersteunt ondertiteling door middel van gehoste WebVTT-bestanden. Bijschriften die met deze parameter worden opgegeven, zijn van toepassing op de video die als eerste in mediasets wordt weergegeven. volgende video&#39;s worden zonder bijschriften afgespeeld. Overlappende cues en gebieden worden niet ondersteund. Ondersteunde operatoren voor actiepunten:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Sleutel </p> </th> 
   <th colname="col2" class="entry"> <p>Naam </p> </th> 
   <th colname="col3" class="entry"> <p>Waarden </p> </th> 
   <th colname="col4" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>uitlijnen testen </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end </span> </p> </td> 
   <td colname="col4"> <p> Hiermee bepaalt u de uitlijning van tekst. </p> <p>Standaard is <span class="codeph"> midden </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>tekstpositie </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage van inzet in de component VideoPlayer voor het begin van de bijschrifttekst. </p> <p>De standaardwaarde is <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>lijngrootte </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentage van videobreedte dat wordt gebruikt voor bijschriften. </p> <p>De standaardwaarde is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>lijnpositie </p> </td> 
   <td colname="col3"> <p> 0%-100%|geheel getal </p> </td> 
   <td colname="col4"> <p> Bepaalt de regelpositie op de pagina. </p> <p>Als de waarde wordt uitgedrukt als een geheel getal zonder procentteken, is dit het aantal regels vanaf de bovenkant waar de tekst wordt weergegeven. </p> <p>Als de waarde wordt uitgedrukt als een percentage-het procentteken het laatste teken is, wordt de bijschrifttekst weergegeven als dat percentage in het weergavegebied. </p> <p>De standaardwaarde is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Houd er rekening mee dat als er andere WebVTT-functies aanwezig zijn in het WebVTT-bestand, deze functies niet worden ondersteund. de ondertiteling wordt echter niet onderbroken.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> bestand </span></span> </p> </td> 
   <td colname="col2"> <p> Hiermee wordt een URL of pad naar WebVTT-bijschriftinhoud opgegeven. Het WebVTT-bestand wordt geleverd door Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Hiermee geeft u de standaardondertitelingsstatus op. </p> <p>Ingeschakeld is <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschappen {#section-10ee45d637134e0fbcd943c62578cb78}

Optioneel.

## Standaard {#section-d411e450028c460392cb8508f8ccc5d9}

Geen.

## Voorbeeld {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```

