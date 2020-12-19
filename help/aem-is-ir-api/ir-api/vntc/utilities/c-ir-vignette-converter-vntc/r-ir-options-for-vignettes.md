---
description: De volgende opties bepalen de verwerking van vignetbestanden. Ze worden genegeerd als sourceFile geen vignet is.
seo-description: De volgende opties bepalen de verwerking van vignetbestanden. Ze worden genegeerd als sourceFile geen vignet is.
seo-title: Opties voor vignetten
solution: Experience Manager
title: Opties voor vignetten
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Opties voor vignetten{#options-for-vignettes}

De volgende opties bepalen de verwerking van vignetbestanden. Ze worden genegeerd als sourceFile geen vignet is.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Hiermee maakt u een XML-bestand dat de objecthiërarchie vertegenwoordigt, inclusief de geselecteerde objectkenmerken. De inhoud van het bestand is gelijk aan de inhoud die wordt geretourneerd door de opdracht <span class="codeph"> req=contents</span>. Het bestand heeft dezelfde naam als het bronbestand, maar met het achtervoegsel <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Snijd het vignet uit voordat u het schaalt. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> yis de linkerbovenhoek van de uitsnijdrechthoek en  <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> </span></span> is de grootte van de uitsnijdrechthoek. Waarden zijn pixelcoördinaten ten opzichte van de weergave-afbeelding met volledige resolutie van het bronvignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Snijd het vignet uit voordat u het schaalt. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> synchroniseert de linkerbovenhoek van de uitsnijdrechthoek en de  <span class="codeph"><span class="varname"> breedte</span>,<span class="varname"> </span></span> retourneert de grootte van de uitsnijdrechthoek. Waarden worden genormaliseerd ten opzichte van de weergaveafbeelding van het bronvignet en moeten liggen tussen 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> width en  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinmust be not greater than 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -inbedmateriaal</span> </p></td> 
  <td class="stentry"> <p>Ingesloten materialen in het uitvoervignet houden. Standaard worden materialen verwijderd uit het uitvoervignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Een of meer uitvoervignethoogten in pixels. Genegeerd als -info wordt gespecificeerd. <span class="varname"> De waarde </span> kan 0 zijn, wat de breedte van het invoervignet aangeeft. Zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignetschaling</a> voor gedetailleerde informatie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Het uitnemen van het afbeeldingskaartbestand uit het vignet inschakelen. De kaartgegevens worden geschreven naar een HTML-bestand dat alleen een <span class="codeph"> &lt;map&gt;</span>-element bevat. Het uitvoerbestand krijgt dezelfde naam als het uitvoerafbeeldingsbestand, maar met het achtervoegsel <span class="filepath"> .htm</span>. Er wordt een waarschuwingsbericht gegenereerd en er wordt geen bestand gemaakt als de opdracht is opgegeven maar er geen kaartgegevens aanwezig zijn in het vignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Hiermee wordt een kopie van het ICC-profiel dat is ingesloten in het vignet, opgeslagen naar een bestand. Er wordt een waarschuwingsbericht gegenereerd en er wordt geen ICC-profielbestand gemaakt als de opdracht is opgegeven maar er geen ICC-profiel aanwezig is in het vignet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -piramide</span> </p></td> 
  <td class="stentry"> <p>Hiermee maakt u een piramidevignet. Vereist wanneer gerenderde afbeeldingen worden weergegeven met Scene7-zoomviewers. Zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignetschaling</a> voor aanvullende informatie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Beperking van pixelbreedte en -hoogte voor de miniatuurafbeelding. Indien opgegeven, wordt een JPEG-afbeelding gegenereerd die niet breder en niet groter is dan <span class="varname"> ival</span> uit de afbeelding van de vignetweergave, een deelvensterafbeelding van het stijlenbestand van het kabinet of de verlichtingskaart van de eerste stijl in het stijlbestand van de vensterbedekkingen. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Een of meer uitvoervignetbreedten in pixels. Genegeerd als <span class="codeph"> -info</span> wordt gespecificeerd. <span class="varname"> De waarde </span> kan 0 zijn, wat de hoogte van het invoervignet aangeeft. Zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignetschaling</a> voor gedetailleerde informatie. </p></td> 
 </tr> 
</table>

