---
description: De IPS Dienst van het Web wordt gesteund door een reeks documenten van WSDL (de Taal van de Beschrijving van de Diensten van het Web) die van om het even welke IPS installatie worden betreden waarop de IPS component van de Dienst van het Web geïnstalleerd is. Elke IPS API-release bevat een nieuw WSDL-bestand dat verwijst naar een versioned doel-XML-naamruimte. Eerdere WSDL-naamruimteversies worden ook ondersteund voor achterwaartse compatibiliteit met bestaande toepassingen.
seo-description: De IPS Dienst van het Web wordt gesteund door een reeks documenten van WSDL (de Taal van de Beschrijving van de Diensten van het Web) die van om het even welke IPS installatie worden betreden waarop de IPS component van de Dienst van het Web geïnstalleerd is. Elke IPS API-release bevat een nieuw WSDL-bestand dat verwijst naar een versioned doel-XML-naamruimte. Eerdere WSDL-naamruimteversies worden ook ondersteund voor achterwaartse compatibiliteit met bestaande toepassingen.
seo-title: IPS Web Service WSDL-versies
solution: Experience Manager
title: IPS Web Service WSDL-versies
topic: Scene7 Image Production System API
uuid: 3443bb91-1663-4686-b20a-94c372f0026e
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '1021'
ht-degree: 0%

---


# IPS Web Service WSDL-versies{#ips-web-service-wsdl-versions}

De IPS Dienst van het Web wordt gesteund door een reeks documenten van WSDL (de Taal van de Beschrijving van de Diensten van het Web) die van om het even welke IPS installatie worden betreden waarop de IPS component van de Dienst van het Web geïnstalleerd is. Elke IPS API-release bevat een nieuw WSDL-bestand dat verwijst naar een versioned doel-XML-naamruimte. Eerdere WSDL-naamruimteversies worden ook ondersteund voor achterwaartse compatibiliteit met bestaande toepassingen.

## WSDL-toegang {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Open de Scene7 WSDL&#39;s zoals hieronder wordt weergegeven.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

De standaardwaarde voor `<IPS_webapp>` is `scene7`.

**Servicelocatie**

De dienst URL wordt gespecificeerd in de dienstsectie van het IPS document van WSDL van de Dienst van het Web. De service-URL heeft doorgaans de volgende notatie:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Toegang tot URL&#39;s voor Scene7-regio&#39;s**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geografische locatie </p> </th> 
   <th colname="col2" class="entry"> <p>Productie-URL </p> </th> 
   <th colname="col3" class="entry"> <p>Staging-URL (gebruik voor ontwikkeling en testen voorafgaand aan de productie) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Noord-Amerika </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Midden-Oosten, Azië </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Azië Stille Oceaan </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ondersteunde WSDL&#39;s {#section-ebbba69880f94e9c823f1147974eb404}

Herinner me, kunt u uw code moeten wijzigen als u eigenschappen in de recentste versie van IPS API wilt gebruiken. IPS API steunt WSDLs voor de volgende versies:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API-releaseversie </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API-naamruimte </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2014-04-03.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2013-02-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2012-02-14.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2010-01-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2009-07-31.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2008-09-10.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IPpsApi-2008-01-15.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl  </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bestaande toepassingen die moeten worden aangepast om nieuwe functies te kunnen gebruiken, moeten een upgrade uitvoeren naar de nieuwste API-versie en moeten mogelijk wijzigingen aanbrengen in bestaande code. Zie het veranderingslogboek voor details.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Bindingen**

De IPS API Dienst van het Web steunt slechts een band van de ZEEP.

**Ondersteunde transporten**

De IPS API band van de ZEEP steunt slechts het vervoer van HTTP. Maak alle verzoeken van de ZEEP gebruikend de methode van de POST HTTPS.

**Koptekst van SOAP-actie**

Als u een aanvraag wilt verwerken, stelt u de HTTP-header van SOAPAction in op de naam van de gevraagde bewerking. Het attribuut van de verrichtingsnaam in de WSDL bindende sectie specificeert de naam.

**Berichtindeling**

De document/letterlijke stijl wordt gebruikt voor alle input en outputberichten met types die op de definitietaal van het Schema van XML ( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/)) worden gebaseerd en in het dossier van WSDL worden gespecificeerd. Alle typen vereisen gekwalificeerde namen met gebruik van de naamruimtewaarde van het doel die in het WSDL-bestand is opgegeven.

**Verificatie aanvragen**

De aangewezen methode om authentificatiegeloofsbrieven in API verzoeken over te gaan is het `authHeader` element zoals die in IPS API WSDL wordt bepaald te gebruiken.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Velden**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Naam </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user  </span> </p> </td> 
   <td colname="col2"> <p> Geldige IPS-gebruikers-e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password  </span> </p> </td> 
   <td colname="col2"> <p>Wachtwoord voor gebruikersaccount. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> landinstelling  </span> </p> </td> 
   <td colname="col2"> <p> Optionele landinstelling voor aanvraag. Zie <b>Landinstelling</b> voor meer informatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName  </span> </p> </td> 
   <td colname="col2"> <p> Toepassingsnaam aanroepen. Deze parameter is optioneel, maar u wordt aangeraden deze in alle aanvragen op te nemen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion  </span> </p> </td> 
   <td colname="col2"> <p> Toepassingsversie aanroepen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse  </span> </p> </td> 
   <td colname="col2"> <p> Optionele markering om gzip-compressie van XML-reactie in of uit te schakelen. Standaard worden de reacties gecomprimeerd met gzip als de HTTP-header voor acceptatie en codering ondersteuning voor gzip aangeeft. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> errorHttpStatusCode  </span> </p> </td> 
   <td colname="col2"> <p> Optionele parameter om de HTTP-statuscode voor foutreacties te negeren. Standaard retourneren de foutreacties HTTP-statuscode 500 (Interne serverfout). Sommige clientplatforms, waaronder Adobe Flash, kunnen de hoofdtekst van de reactie niet lezen, tenzij de statuscode 200 (OK) wordt geretourneerd. </p> </td> 
  </tr> 
 </tbody> 
</table>

Het element `authHeader` wordt altijd gedefinieerd in de naamruimte `http://www.scene7.com/IpsApi/xsd`, ongeacht de API-versie.

Hieronder ziet u een voorbeeld van het gebruik van het element `authHeader` in een SOAP-koptekst voor een aanvraag:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Andere methoden voor aanvraagverificatie**

Als het om wat voor reden dan ook niet mogelijk is voor uw cliënttoepassing om de `authHeader` kopbal van de ZEEP over te gaan, kunnen de API verzoeken geloofsbrieven ook specificeren gebruikend de Basisauthentificatie van HTTP (zoals gespecificeerd in RFC 2617).

Voor HTTP Basic-verificatie moet de HTTP-headersectie van elke SOAP-POST-aanvraag een header van het formulier bevatten:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Waar `base64()` standaardBase64 het coderen toepast, `<IPS_user_email>` is het e-mailadres van een geldige IPS gebruiker, en `<password>` is het wachtwoord van de gebruiker.

Verzend de koptekst voor autorisatie op voorhand met het eerste verzoek. Als de aanvraag geen verificatiereferenties bevat, reageert `IpsApiService` niet met een statuscode van `401 (Unauthorized)`. In plaats daarvan, is een statuscode van `500 (Internal Server Error)` teruggekeerd met een de foutenlichaam die van de ZEEP dat verklaart dat het verzoek niet kon worden voor authentiek verklaard.

Vóór IPS 3.8, werd de authentificatie via de kopbal van de ZEEP uitgevoerd gebruikend `AuthUser` en `AuthPassword` elementen in namespace `http://www.scene7.com/IpsApi`. Bijvoorbeeld:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Deze stijl wordt nog steeds ondersteund voor achterwaartse compatibiliteit, maar is vervangen door het element `authHeader`.

**Verzoek om toestemming**

Nadat de geloofsbrieven van de bezoeker voor authentiek worden verklaard, wordt het verzoek gecontroleerd om ervoor te zorgen dat de bezoeker wordt gemachtigd om de gevraagde verrichting uit te voeren. De vergunning is gebaseerd op de gebruikersrol van de bezoeker en kan ook vereisen controlerend het doelbedrijf, doelgebruiker, en andere verrichtingsparameters. Bovendien moeten de gebruikers van het Portaal van het Beeld tot een Groep met de vereiste toestemmingen behoren om bepaalde omslag en activaverrichtingen uit te voeren. De sectie Verrichtingen verwijst naar de vergunningsvereisten voor elke vluchtuitvoering.

**Voorbeeld van SOAP-verzoek en -antwoord**

In het volgende voorbeeld wordt een volledige `addCompany`-bewerking getoond, inclusief HTTP-headers:

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

En de corresponderende reactie:

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP-fouten**

Wanneer een verrichting een uitzonderingsvoorwaarde ontmoet, is een fout van de ZEEP teruggekeerd als lichaam van het bericht van de ZEEP in plaats van de normale reactie. Bijvoorbeeld, als een niet-admin gebruiker probeert om het vorige `addCompany` verzoek te verzenden, is de volgende reactie teruggekeerd:

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```

