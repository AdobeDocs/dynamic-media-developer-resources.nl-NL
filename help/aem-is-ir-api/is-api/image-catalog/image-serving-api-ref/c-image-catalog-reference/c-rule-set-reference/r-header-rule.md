---
description: HTTP-responsheader-element. Optioneel in elementen <rule>.
seo-description: HTTP-responsheader-element. Optioneel in elementen <rule>.
seo-title: header
solution: Experience Manager
title: header
topic: Scene7 Image Serving - Image Rendering API
uuid: 89ec0f27-fc12-47c2-b9dd-e0ee768587b5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# header{#header}

HTTP-responsheader-element. Optioneel in `<rule>` elementen.

## Attributen {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;**: Vereist. Geeft de naam van de HTTP-header op.

**`Action`= &quot;set&quot;|`"add"`**: Optioneel. Standaard is dit`"set"`de vervanging van de huidige headerwaarde. Geef`"add"`op of u de koptekstwaarde wilt toevoegen, gescheiden door een komma.

## Gegevens {#section-a387f541396c49d99c29692a38032914}

Waarde koptekst.

## Beschrijving {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Hiermee kunt u nieuwe HTTP-antwoordheaders toevoegen en waarden van vooraf gedefinieerde kopteksten toevoegen of vervangen. Namen en waarden moeten voldoen aan de HTTP-normen. Er wordt geen aanvullende codering toegepast.

U kunt vervangende variabelen voor afbeeldingsservers gebruiken in de koptekstnaam en de koptekstwaarde. Hierdoor kunt u beide tekenreeksen vanuit de aanvraag besturen.

## Voorbeeld {#section-cb5b738b9b93407cb2f4d35af3e59c02}

De volgende regel past een aangepaste koptekst toe wanneer de koptekstwaarde in de aanvraag is opgegeven als een variabele:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Deze regel wordt geactiveerd door de volgende aanvraag, die de HTTP-antwoordheader instelt `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
