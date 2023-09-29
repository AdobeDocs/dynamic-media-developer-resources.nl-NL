---
title: header
description: HTTP response header element. Optioneel in <rule> elementen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# header{#header}

HTTP response header element. Optioneel in `<rule>` elementen.

## Attributen {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Vereist. Geeft de naam van de HTTP-header op.

**`Action`= &quot;set&quot; |`"add"`**: Optioneel. Standaard is `"set"`, die de huidige headerwaarde vervangt. Opgeven `"add"` zodat u de koptekstwaarde kunt toevoegen, gescheiden met een komma.

## Gegevens {#section-a387f541396c49d99c29692a38032914}

Waarde koptekst.

## Beschrijving {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Hiermee kunt u nieuwe HTTP-antwoordheaders toevoegen en waarden van vooraf gedefinieerde koppen toevoegen of vervangen. Namen en waarden moeten voldoen aan de HTTP-normen. Er wordt geen aanvullende codering toegepast.

U kunt vervangende variabelen voor afbeeldingsservers gebruiken in de koptekstnaam en de koptekstwaarde. Hierdoor kunt u beide tekenreeksen vanuit de aanvraag besturen.

## Voorbeeld {#section-cb5b738b9b93407cb2f4d35af3e59c02}

De volgende regel past een aangepaste koptekst toe wanneer de koptekstwaarde in de aanvraag is opgegeven als een variabele:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Deze regel wordt geactiveerd door de volgende aanvraag en stelt de HTTP-responsheader in `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
