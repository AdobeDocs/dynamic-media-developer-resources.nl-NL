---
description: HTTP-responsheader-element. Optioneel in elementen <rule>.
solution: Experience Manager
title: header
feature: Dynamic Media Classic, SDK/API
role: Ontwikkelaar,zakelijke praktiserer
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# header{#header}

HTTP-responsheader-element. Optioneel in `<rule>`-elementen.

## Kenmerken {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*tekst*&quot;** : Vereist. Geeft de naam van de HTTP-header op.

**`Action`= &quot;set&quot; |`"add"`**: Optioneel. De standaardwaarde is `"set"`, die de huidige headerwaarde vervangt. Geef `"add"` op om de koptekstwaarde toe te voegen, gescheiden met een komma.

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

Deze regel wordt teweeggebracht door het volgende verzoek, die de HTTP- reactiekop `Edge-Control::no-store` plaatsen:

`http://server/is/image/cat/id?$Edge-Control=no-store`
