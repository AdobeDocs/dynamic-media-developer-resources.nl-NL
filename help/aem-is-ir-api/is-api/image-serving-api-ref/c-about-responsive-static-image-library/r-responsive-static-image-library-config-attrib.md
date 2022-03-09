---
description: De attributen van de configuratie worden bepaald als attributen direct op een element IMG dat de Responsieve bibliotheek van het Beeld beheert. Elke afbeelding kan een eigen set kenmerken hebben.
solution: Experience Manager
title: Command reference - Configuration attributes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Command reference - Configuration attributes{#command-reference-configuration-attributes}

De attributen van de configuratie worden bepaald als attributen direct op een element IMG dat de Responsieve bibliotheek van het Beeld beheert. Elke afbeelding kan een eigen set kenmerken hebben.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Optioneel.

URL naar de afbeelding die wordt weergegeven in de afbeeldingsserver. Als de URL niet aanwezig is, gebruikt de bibliotheek de waarde die is ingesteld in `src` kenmerk als fallback. Dit kenmerk dient voor de eerste afbeelding en de dynamische afbeelding die in de bibliotheek met responsieve afbeeldingen vanaf verschillende locaties wordt beheerd.

**Voorbeeld**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Indien `data-src` is ingesteld, `src` is optioneel en kan elke URL bevatten die u wilt toevoegen. Het kan bijvoorbeeld een URL bevatten naar dezelfde afbeelding die op afbeeldingsserver is gebaseerd en die door de bibliotheek wordt gebruikt. Of het formulier kan een tijdelijke aanduiding voor GIFFEN of zelfs een gegevens-URI bevatten om te voorkomen dat er bij het opstarten een extra tijdelijke conversie van de server plaatsvindt.

Indien `data-src` niet is ingesteld, `src` is verplicht en moet een URL bevatten naar de afbeelding die in Image Serving wordt weergegeven.

**Voorbeeld**

De gegevens-URI gebruiken voor de `src` kenmerk en URL voor afbeeldingsservice voor de `data-src` kenmerk:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## data-breakpoints {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Een door komma&#39;s gescheiden lijst met onderbrekingspunten en optioneel gevolgd door een dubbele punt ( `:`) en opdrachten of Voorinstellingen afbeelding voor Beeldserver. Elk onderbrekingspunt is een waarde van de beeldbreedte die in logische CSS pixel wordt bepaald. De bibliotheek laadt de afbeelding met de dichtstbijzijnde grotere waarde uit de lijst en verkleint deze op de client, zodat deze overeenkomt met de breedte van de CSS-afbeelding bij uitvoering. (Als u op een scherm met hoge dichtheid werkt, vertegenwoordigen afbeeldingsuitvoeringen die vanaf de server worden geladen, onderbrekingspuntwaarden vermenigvuldigd met de pixelverhouding van het apparaat).

Voor elk onderbrekingspunt in de lijst kunt u een of meer opdrachten of namen van voorinstellingen voor afbeeldingen definiëren. Dergelijke extra parameters worden alleen toegepast op de afbeelding als dit specifieke onderbrekingspunt momenteel actief is.

U kunt elke ondersteunde opdracht Beeldverwerking gebruiken, behalve de weergaveopdrachten die invloed hebben op de grootte van de reactieafbeelding, zoals `wid=`, `hei=`, of `scl=`. Dezelfde beperking geldt voor voorinstellingen afbeelding: Een voorinstelling voor afbeeldingen die wordt gebruikt in de bibliotheek met responsieve afbeeldingen mag dergelijke opdrachten niet bevatten.

Meerdere opdrachten voor het leveren van afbeeldingen of namen van voorinstellingen voor afbeeldingen worden gescheiden met &quot; `&`&quot; teken. Als de waarde van een opdracht Beeldbewerking komma&#39;s bevat, wordt deze komma vervangen door `%2C`. Namen van voorinstellingen voor afbeelding worden omwikkeld in dollartekens ( `$`).

**Voorbeelden**

**Alleen onderbrekingspunten gebruiken**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Opdrachten Afbeeldingsservice gebruiken**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Voorinstellingen afbeelding gebruiken**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Voorinstellingen afbeelding gebruiken en opdrachten Afbeeldingsservice**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## gegevensmodus {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

De volgende twee modi voor slim uitsnijden zijn beschikbaar in AEM 6.4 en hoger en Dynamic Media Viewers 5.9 en hoger:

* **Handmatig** - door de gebruiker gedefinieerde onderbrekingspunten en de bijbehorende opdrachten in Image Service worden gedefinieerd binnen een kenmerk in het afbeeldingselement.
* **Slim uitsnijden** - berekende slimme uitsnijdingen worden automatisch opgehaald van de leveringsserver. De beste vertoning wordt geselecteerd gebruikend de runtime grootte van het beeldelement.

Als u de modus Slim uitsnijden wilt gebruiken, stelt u de optie `data-mode` kenmerk naar `smart crop`.

**Voorbeeld**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Het gekoppelde afbeeldingselement verzendt een `s7responsiveViewer` gebeurtenis tijdens runtime wanneer het onderbrekingspunt verandert.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
