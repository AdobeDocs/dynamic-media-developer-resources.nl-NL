---
description: De volgende opties kunnen worden toegepast, ongeacht het type sourceFile.
seo-description: De volgende opties kunnen worden toegepast, ongeacht het type sourceFile.
seo-title: Algemene opties
solution: Experience Manager
title: Algemene opties
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Algemene opties{#common-options}

De volgende opties kunnen worden toegepast, ongeacht het type sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath- <span class="varname"> tekenreeks </span></span> </p> </td> 
  <td class="stentry"> <p>Map waarin uitvoerbestanden moeten worden geplaatst (inclusief het logbestand, als <span class="codeph"> -log </span> is opgegeven). Dit kan een absoluut pad zijn of een relatief pad ten opzichte van de huidige werkmap. De mappenhiërarchie wordt gemaakt als deze niet bestaat. Is niet van toepassing op het dossier met <span class="codeph"> -log wordt gespecificeerd </span>. Als u geen waarde opgeeft, worden uitvoerbestanden naar de map geschreven waarin <span class="varname"> het bronbestand </span> zich bevindt. Als <span class="varname"> destFile </span> wordt gespecificeerd, zal het altijd aan die plaats worden geschreven, en <span class="codeph"> -destpath is </span> slechts op de secundaire outputdossiers van toepassing. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Indien opgegeven, wordt de (eerste) weergaveafbeelding geëxtraheerd uit het vignet, een geschikte paneelafbeelding uit een kabinetsstijl of de eerste belichtingsafbeelding van een vensterbedekkingsstijl. De geëxtraheerde afbeelding wordt opgeslagen als een TIFF-bestand met volledige resolutie. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Voorkomt het genereren van doelbestanden. Nuttig om kenmerken snel uit <span class="varname"> bronbestand te extraheren </span>. Alleen de optionele miniaturen ( <span class="codeph"> -thumbwidth </span>), afbeeldingen ( <span class="codeph"> -image </span>) en logbestanden ( <span class="codeph"> -log </span>) worden gegenereerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> jpegquality <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Hiermee selecteert u JPEG-codering met verlies voor RGB- en grijswaardenafbeeldingsgegevens die zijn ingesloten in het uitvoerbestand in plaats van PNG zonder gegevensverlies. Afbeeldingen met alfa (RGBA) worden altijd opgeslagen met PNG-codering. <span class="varname"> ival </span> geeft de JPEG-kwaliteit aan (1...100); 85 of hoger wordt aanbevolen. De standaardwaarde is <span class="codeph"> -jpegquality 0 </span>, waarmee PNG-codering wordt geselecteerd. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> -pad </span></span> </p> </td> 
  <td class="stentry"> <p>Hiermee maakt u een logbestand met het opgegeven pad/de opgegeven naam. De volledige paden van alle uitvoerbestanden die naar de doelmap worden geschreven, worden naar het logbestand geschreven, evenals enkele aanvullende instellingen, zoals versiegegevens en eventuele waarschuwingen of fouten (zie <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Uitvoer </a> voor meer informatie). Er wordt geen logbestand gemaakt als <span class="codeph"> -log </span> niet is opgegeven. in dit geval wordt alle tekstuitvoer naar <span class="codeph"> stdout geschreven </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Verlaag de prioriteit van het <span class="filepath"> vntc- </span> proces. Dit kan worden gebruikt zodat <span class="filepath"> vntc een volledige cpu </span> niet zal overnemen terwijl het verwerken van een vignet. Hierdoor kan het besturingssysteem meer tijd geven aan andere, belangrijker processen. <span class="varname"> ival </span> geeft het percentage met de laagste prioriteit aan (0..100). Het gebrek is <span class="codeph"> - lagere prioriteit 0 </span>, die niet de prioriteit van het <span class="filepath"> vntc </span> proces vermindert. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Geef de maximale hoeveelheid geheugen op die vntc <span class="filepath"> </span> mag gebruiken in bytes. Wanneer <span class="filepath"> vntc de maximale geheugenlimiet </span> bereikt, wordt de verwerking gestopt en wordt een fout gegenereerd. <span class="varname"> ival </span> geeft de maximale geheugenlimiet in bytes aan (0.. 3.758.096.384 (3,5 GB)). Wanneer <span class="varname"> ival 0 </span> is, wordt de maximale geheugenlimiet uitgeschakeld. De standaardwaarde is <span class="codeph"> -maxmem 3221225472 </span>, wat een maximumgeheugenlimiet van 3 GB betekent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Hiermee geeft u het scheidingsteken tussen de bestandsnaam en het achtervoegsel voor grootte/resolutie op voor automatisch gegenereerde namen van uitvoerbestanden. Heeft als standaardwaarde "-" (indien niet opgegeven). Wordt genegeerd als <span class="varname"> destFile </span> - of <span class="codeph"> -info </span> is opgegeven. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Hiermee kunt u afbeeldingen waarvan het aantal pixels tijdens de verwerking is gewijzigd (geschaald), verscherpen. Dit is alleen van toepassing op miniatuurverscherping in het geval van bestanden met kabinetsstijlen. </p> <p>Geef 0 op om verscherpen uit te schakelen (standaard), 1 om normale verscherping in te schakelen, 2 om onscherp maskeren alleen voor helderheid in te schakelen, of 3 om onscherp maskeren in te schakelen voor elke kleurcomponent. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Hiermee stelt u het logniveau in. De standaardwaarde is 1, die alle informatie-, waarschuwings- en foutberichten uitvoert. Ingesteld op 0 om alle foutberichten behalve uit te schakelen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> bedrag </span> <span class="varname"> straaldrempel </span> <span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>Hiermee stelt u de parameters voor onscherp maskeren in. Genegeerd als <span class="codeph"> -sharpen </span> is ingesteld op 0 of 1; vereist als <span class="codeph"> -sharpen </span> is ingesteld op 2 of 3. <span class="varname"> Het bedrag </span> is een reële waarde in waaier 0.0..500.0, <span class="varname"> straal </span> is een echte waarde in waaier 0.0...10.0, en de <span class="varname"> drempel </span> is een geheel tussen 0 en 255. Zie de beschrijving van <span class="codeph"> op_usm= </span> in de Verwijzing van het Protocol van de Beelddienst voor extra informatie. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Controleer of het opgegeven vignet een juist productievenster is. <span class="varname"> ival </span> staat voor de minimale bestandsversie van het vignet. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Bestandsversie voor het uitvoerbestand. Indien opgegeven, moet dit 0 of een geldige versie van het vignetbestand zijn (niet groter dan de standaardbestandsversie). Indien ingesteld op 0 of niet opgegeven, wordt het uitvoerbestand gemaakt met de meest recente bestandsversie. Genegeerd als <span class="codeph"> -info </span> is opgegeven. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Retourneert versiegegevens voor dit hulpprogramma. Geef opties op zonder bestandsnaam en andere opties. </p> </td> 
 </tr> 
</table>

