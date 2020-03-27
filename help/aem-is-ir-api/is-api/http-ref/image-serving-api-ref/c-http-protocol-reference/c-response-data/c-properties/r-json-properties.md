---
description: Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.
seo-description: Als jsonp wordt gespecificeerd als reactie formaat, worden de antwoordgegevens geformatteerd gebruikend JSONP (de Nota van de Objecten JavaScript met het Opvullen), verpakt in een functie JavaScript vraag.
seo-title: JSONP-eigenschappen
solution: Experience Manager
title: JSONP-eigenschappen
topic: Scene7 Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

De `s7jsonResponse` JavaScript-functie moet door de client worden gedefinieerd. In zijn eenvoudigste vorm kan de functie er als volgt uitzien:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Verzoeken die JSONP reactieformaat steunen laten u de naam van de callback manager specificeren JS gebruikend de uitgebreide syntaxis van `req=` parameter:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` is de naam van de manager JS die in de reactie JSONP aanwezig is. Alleen a-z, A-Z en 0-9 tekens zijn toegestaan. Optioneel. Standaard is dit `s7jsonResponse`.

Het pakket van Kijkers die van het Beeld Scene7 Beeld Dient omvat een nut om JSONP-Geformatteerde gegevens van het Serven van het Beeld te verzoeken en te ontleden.

Zie [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) voor meer informatie over het formaat JSONP.

Surf naar [www.json.org](http://www.json.org) voor meer informatie over de JSON-indeling.

Zie ook [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
