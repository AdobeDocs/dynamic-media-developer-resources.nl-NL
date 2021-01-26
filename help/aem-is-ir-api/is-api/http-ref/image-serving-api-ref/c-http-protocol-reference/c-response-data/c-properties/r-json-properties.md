---
description: Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.
seo-description: Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.
seo-title: JSONP-eigenschappen
solution: Experience Manager
title: JSONP-eigenschappen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# JSONP-eigenschappen{#jsonp-properties}

Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.

De client kan een optionele unieke aanvraag-id ( *`reqId`*) opgeven, die in de reactie wordt geretourneerd en waarmee de client meerdere asynchroon ontvangen reacties kan onderscheiden. Een typische reactie heeft de volgende algemene structuur:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

De JavaScript-functie `s7jsonResponse` moet door de client worden gedefinieerd. In zijn eenvoudigste vorm kan de functie er als volgt uitzien:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. De standaardwaarde is `s7jsonResponse`.

Het Dynamic Media Image Serving Viewers-pakket bevat een hulpprogramma voor het aanvragen en parseren van gegevens met de JSONP-indeling van Image Serving.

Zie [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) voor meer informatie over het formaat JSONP.

Zie [www.json.org](http://www.json.org) voor meer informatie over de JSON-indeling.

Zie ook [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
