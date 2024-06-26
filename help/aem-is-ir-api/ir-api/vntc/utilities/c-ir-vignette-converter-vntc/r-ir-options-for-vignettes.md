---
description: De volgende opties bepalen de verwerking van vignetbestanden. Ze worden genegeerd als sourceFile geen vignet is.
solution: Experience Manager
title: Opties voor vignetten
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Opties voor vignetten{#options-for-vignettes}

De volgende opties bepalen de verwerking van vignetbestanden. Ze worden genegeerd als sourceFile geen vignet is.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Hiermee maakt u een XML-bestand dat de objecthiërarchie vertegenwoordigt, inclusief de geselecteerde objectkenmerken. De inhoud van het bestand is gelijk aan de inhoud die wordt geretourneerd door de <span class="codeph"> req=contents</span> gebruiken. Het bestand heeft dezelfde naam als het bronbestand, maar met een <span class="filepath"> .xml</span> achtervoegsel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-uitsnijden <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> winderig</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Snijd het vignet uit voordat u het schaalt. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> de linkerbovenhoek van de snijrechthoek is, en <span class="codeph"><span class="varname"> winderig</span>,<span class="varname"> hei</span></span> is de grootte van de uitsnijdrechthoek. Waarden zijn pixelcoördinaten ten opzichte van de weergave-afbeelding met volledige resolutie van het bronvignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> brein</span><span class="varname"> heek</span></span> </p> </td> 
  <td class="stentry"> <p>Snijd het vignet uit voordat u het schaalt. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> de linkerbovenhoek van de snijrechthoek is, en <span class="codeph"><span class="varname"> brein</span>,<span class="varname"> heek</span></span> is de grootte van de uitsnijdrechthoek. Waarden worden genormaliseerd ten opzichte van de weergaveafbeelding van het bronvignet en moeten liggen tussen 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> brein</span></span> en <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> heek</span></span> mag niet groter zijn dan 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -inbedmateriaal</span> </p></td> 
  <td class="stentry"> <p>Ingesloten materialen in het uitvoervignet houden. Standaard worden materialen verwijderd uit het uitvoervignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>Een of meer uitvoervignethoogten in pixels. Genegeerd als -info wordt gespecificeerd. <span class="varname"> ivaal</span> kan 0 zijn, wat de breedte van het invoervignet aangeeft. Zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignet schalen</a> voor nadere informatie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Het uitnemen van het afbeeldingskaartbestand uit het vignet inschakelen. De kaartgegevens worden naar een HTML-bestand geschreven dat alleen een <span class="codeph"> &lt;map&gt;</span> element. Het uitvoerbestand krijgt dezelfde naam als het uitvoerafbeeldingsbestand, maar met een <span class="filepath"> .htm</span> achtervoegsel. Er wordt een waarschuwingsbericht gegenereerd en er wordt geen bestand gemaakt als de opdracht is opgegeven maar er geen kaartgegevens aanwezig zijn in het vignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Hiermee wordt een kopie van het ICC-profiel dat is ingesloten in het vignet, opgeslagen naar een bestand. Er wordt een waarschuwingsbericht gegenereerd en er wordt geen ICC-profielbestand gemaakt als de opdracht is opgegeven maar er geen ICC-profiel aanwezig is in het vignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -piramide</span> </p></td> 
  <td class="stentry"> <p>Hiermee maakt u een piramidevignet. Vereist wanneer gerenderde afbeeldingen worden weergegeven met Dynamic Media-zoomviewers. Zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignet schalen</a> voor aanvullende informatie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ivaal</span></span> </p></td> 
  <td class="stentry"> <p>Beperking van pixelbreedte en -hoogte voor de miniatuurafbeelding. Indien opgegeven, een JPEG-afbeelding die niet breder en niet groter is dan <span class="varname"> ivaal</span> wordt gegenereerd op basis van de afbeelding van de vignetweergave, een deelvensterafbeelding van het stijlenbestand van het kabinet of de verlichtingskaart van de eerste stijl in het stijlbestand van de vensterbedekkingen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ivaal</span> *[,<span class="varname"> ivaal</span>]</span> </p></td> 
  <td class="stentry"> <p>Een of meer uitvoervignetbreedten in pixels. Genegeerd als <span class="codeph"> -info</span> wordt opgegeven. <span class="varname"> ivaal</span> kan 0 zijn, wat de hoogte van het invoervignet aangeeft. Zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignet schalen</a> voor nadere informatie. </p></td> 
 </tr> 
</table>
