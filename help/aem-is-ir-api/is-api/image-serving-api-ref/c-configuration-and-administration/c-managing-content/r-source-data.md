---
description: Bestanden met brongegevens van afbeeldingsserver bevatten afbeeldings- en maskerbestanden, lettertypen en ICC-profielen.
solution: Experience Manager
title: Brongegevens
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Brongegevens{#source-data}

Bestanden met brongegevens van afbeeldingsserver bevatten afbeeldings- en maskerbestanden, lettertypen en ICC-profielen.

Alle brongegevensdossiers moeten voor de Server van het Beeld toegankelijk zijn. Beeldserver biedt een aantal alternatieven voor het opgeven van de locatie van gegevensbestanden:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
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

Alles `*`rootPath`*` segmenten kunnen leeg, relatief of absoluut zijn.

`*`catalogPath`*` is een absoluut of relatief bestandspad/-naam. `*`requestPath`*` moet een relatief bestandspad/-naam zijn.

`Multiple IS::RootPath` waarden kunnen worden gedefinieerd in ImageServerRegistry.xml (of via de beheerdersinterface). Hierdoor kunnen brongegevensbestanden over meerdere bestandssystemen worden verspreid. De server van het Beeld probeert afwisselende wegen in de gespecificeerde orde tot het gegevensdossier wordt gevonden.

U kunt op elk moment nieuwe gegevensbestanden toevoegen zonder de server te stoppen.
