---
description: Bestanden met brongegevens van afbeeldingsserver bevatten afbeeldings- en maskerbestanden, lettertypen en ICC-profielen.
solution: Experience Manager
title: Brongegevens
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Brongegevens{#source-data}

Bestanden met brongegevens van afbeeldingsserver bevatten afbeeldings- en maskerbestanden, lettertypen en ICC-profielen.

Alle brongegevensdossiers moeten voor de Server van het Beeld toegankelijk zijn. Beeldserver biedt een aantal alternatieven voor het opgeven van de locatie van gegevensbestanden:

`*`install_`*/ *``*/ *`folderPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogus::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> Het relatieve pad naar het afbeeldingsbestand en de naam die zijn opgegeven in een HTTP-aanvraag voor Image Serving</span> </p></td> 
 </tr> 
</table>

De server combineert padsegmenten van rechts naar links totdat een absoluut bestandspad is ingesteld.

Alle `*`rootPath`*` segmenten kunnen lege, relatieve, of absolute wegsegmenten zijn.

`*``*` catalogEen absoluut of relatief bestandspad/-naam. `*``*` requestPathmust be a relative file path/ name.

`Multiple IS::RootPath` waarden kunnen worden gedefinieerd in ImageServerRegistry.xml (of via de beheerdersinterface). Hierdoor kunnen brongegevensbestanden over meerdere bestandssystemen worden verspreid. De server van het Beeld zal afwisselende wegen in de gespecificeerde orde proberen tot het gegevensdossier wordt gevonden.

U kunt op elk moment nieuwe gegevensbestanden toevoegen zonder de server te stoppen.
