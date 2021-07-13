---
description: Bevat de configuratiemontages van de Server van het Beeld.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Bevat de configuratiemontages van de Server van het Beeld.

Wanneer u dit XML-bestand wijzigt, moet u ervoor zorgen dat geldige XML-syntaxis behouden blijft, anders start de Image Server mogelijk niet.

Start de afbeeldingsserver na het bewerken van dit bestand opnieuw om de wijzigingen door te voeren. Alleen de onderstaande elementwaarden worden ondersteund voor wijziging. Bewerk de overige inhoud van dit bestand alleen op advies van de technische ondersteuning van Dynamic Media.

>[!NOTE]
>
>Wijzig de structuur van `<imageserverregistry>` niet, inclusief de volgorde van elementen. Wees voorzichtig als u dit bestand bewerkt, anders kan het zijn dat de Image Server niet kan worden gestart.

In het volgende voorbeeld wordt aangegeven welke elementen kunnen worden gewijzigd. Er zijn andere elementen die niet mogen worden gewijzigd. De volgorde van de onderstaande elementen weerspiegelt niet de volgorde waarin deze in het bestand aanwezig moeten zijn.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Notities {#section-7217f011f69f41e7af4f3983d7776d6f}

Er kunnen meerdere `<RootPath>`-elementen aanwezig zijn (één voor elke brongegevensbestandsmap). De Server van het beeld zoekt de wortelwegen in de orde die wordt gespecificeerd om een bepaald brondossier te vinden.
