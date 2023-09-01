---
title: Algemene opties
description: De volgende opties kunnen worden toegepast, ongeacht het type sourceFile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# Algemene opties{#common-options}

De volgende opties kunnen worden toegepast, ongeacht het type sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Map waarin uitvoerbestanden moeten worden geplaatst (inclusief het logbestand als <span class="codeph"> -log </span> is opgegeven). Dit kan een absoluut pad zijn of een relatief pad naar de huidige werkmap. De maphiërarchie wordt gemaakt als deze niet bestaat, maar is niet van toepassing op het bestand dat is opgegeven met <span class="codeph"> -log </span>. Indien niet opgegeven, worden de uitvoerbestanden naar de map geschreven waarin de <span class="varname"> sourceFile </span> bevindt. Indien <span class="varname"> destFile </span> wordt opgegeven, wordt deze altijd naar die locatie geschreven, en <span class="codeph"> -destpath </span> is alleen van toepassing op de secundaire uitvoerbestanden. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Indien opgegeven, wordt de (eerste) weergaveafbeelding geëxtraheerd uit het vignet, een geschikte paneelafbeelding uit een kabinetsstijl of de eerste belichtingsafbeelding van een vensterbedekkingsstijl. De geëxtraheerde afbeelding wordt opgeslagen als een TIFF-bestand met volledige resolutie. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Voorkomt het genereren van doelbestanden. Nuttig om kenmerken snel te extraheren uit een <span class="varname"> sourceFile </span>. Alleen de optionele miniatuur ( <span class="codeph"> -thumbwidth </span>), afbeelding ( <span class="codeph"> -image </span>) en logbestanden ( <span class="codeph"> -log </span>) gegenereerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ivaal </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee selecteert u JPEG-codering met verlies voor RGB- en grijswaardenafbeeldingsgegevens die zijn ingesloten in het uitvoerbestand in plaats van PNG zonder gegevensverlies. Afbeeldingen met alfa (RGBA) worden altijd opgeslagen met PNG-codering. <span class="varname"> ivaal </span> geeft de kwaliteit van de JPEG aan (1...100); 85 of hoger wordt aanbevolen. De standaardwaarde is <span class="codeph"> -jpegquality 0 </span>, waarin PNG-codering wordt geselecteerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> pad </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee maakt u een logbestand met het opgegeven pad of de opgegeven naam. De volledige paden van alle uitvoerbestanden die naar de doelmap worden geschreven, worden naar het logbestand geschreven en er worden enkele aanvullende instellingen opgegeven, zoals versiegegevens en eventuele waarschuwingen of fouten (zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Uitvoer </a> voor meer informatie). Er wordt geen logbestand gemaakt als <span class="codeph"> -log </span> is niet opgegeven; in dit geval wordt alle tekstuitvoer weggeschreven naar <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -mindere prioriteit <span class="varname"> ivaal </span> </span> </p> </td> 
  <td class="stentry"> <p>Verlaag de prioriteit van de <span class="filepath"> vntc </span> proces. Dit proces kan worden gebruikt zodat <span class="filepath"> vntc </span> neemt niet een volledige CPU over tijdens het verwerken van een vignet. Hierdoor kan het besturingssysteem meer tijd geven aan andere, belangrijker processen. <span class="varname"> ivaal </span> geeft het percentage met lagere prioriteit aan (0..100). De standaardwaarde is <span class="codeph"> -lagere prioriteit 0 </span>, die de prioriteit van de <span class="filepath"> vntc </span> proces. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ivaal </span> </span> </p> </td> 
  <td class="stentry"> <p>De maximale hoeveelheid geheugen opgeven <span class="filepath"> vntc </span> mag worden gebruikt in bytes. Wanneer <span class="filepath"> vntc </span> bereikt de maximale geheugenlimiet, stopt de verwerking en veroorzaakt een fout. De <span class="varname"> ivaal </span> geeft de maximale geheugenlimiet in bytes aan (0.. 3.758.096.384 (3,5 GB). Wanneer <span class="varname"> ivaal </span> 0 is, wordt de maximale geheugenlimiet uitgeschakeld. De standaardwaarde is <span class="codeph"> -maxmem 3221225472 </span>, wat een maximale geheugenlimiet van 3 GB betekent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Hiermee geeft u het scheidingsteken tussen de bestandsnaam en het achtervoegsel voor grootte/resolutie op voor automatisch gegenereerde namen van uitvoerbestanden. Heeft als standaardwaarde "-" (indien niet opgegeven). Genegeerd als <span class="varname"> destFile </span> of <span class="codeph"> -info </span> wordt opgegeven. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ivaal </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee kunt u afbeeldingen waarvan het aantal pixels tijdens de verwerking is gewijzigd (geschaald), verscherpen. Alleen van toepassing op miniatuurverscherping in bestanden in kabinetsstijl. </p> <p>Geef 0 op om verscherpen uit te schakelen (standaard), 1 om normale verscherping in te schakelen, 2 om onscherp maskeren alleen voor helderheid in te schakelen, of 3 om onscherp maskeren in te schakelen voor elke kleurcomponent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Hiermee stelt u het logniveau in. De standaardwaarde is 1, die alle informatie-, waarschuwings- en foutberichten uitvoert. Ingesteld op 0 om alle foutberichten behalve uit te schakelen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> bedrag </span> <span class="varname"> radius </span> <span class="varname"> drempel </span> </span> </p> </td> 
  <td class="stentry"> <p>Hiermee stelt u de parameters voor onscherp maskeren in. Genegeerd als <span class="codeph"> -sharpen </span> is ingesteld op 0 of 1; is vereist als <span class="codeph"> -sharpen </span> wordt ingesteld op 2 of 3. De <span class="varname"> bedrag </span> is een reële waarde in het bereik 0,0...500,0. <span class="varname"> radius </span> is een reële waarde in het bereik 0,0...10,0 en de <span class="varname"> drempel </span> is een geheel getal tussen 0 en 255. Zie de beschrijving van <span class="codeph"> op_usm= </span> in de Verwijzing van het Protocol van de Serving van het Beeld voor extra informatie. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ivaal </span> </span> </p> </td> 
  <td class="stentry"> <p>Controleer of het opgegeven vignet een juist productievenster is. De <span class="varname"> ivaal </span> geeft de minimale bestandsversie van het vignet aan. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ivaal </span> </span> </p> </td> 
  <td class="stentry"> <p>Bestandsversie voor het uitvoerbestand. Als deze is opgegeven, moet deze 0 of een geldige versie van het vignetbestand zijn (niet groter dan de standaardbestandsversie). Indien ingesteld op 0 of niet opgegeven, wordt het uitvoerbestand gemaakt met de meest recente bestandsversie. Genegeerd als <span class="codeph"> -info </span> wordt opgegeven. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Retourneert versiegegevens voor dit hulpprogramma. Geef opties op zonder bestandsnaam en andere opties. </p> </td> 
 </tr> 
</table>
