---
description: Bevat configuratie-instellingen voor servertoezicht.
solution: Experience Manager
title: SupervisorRegistry.xml
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: cc6a16fb-fd70-431f-aad6-adb99d4da062
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# SupervisorRegistry.xml{#supervisorregistry-xml}

Bevat configuratie-instellingen voor servertoezicht.

Zorg dat u bij het bewerken van dit XML-bestand een geldige XML-syntaxis behoudt, anders kan het zijn dat de Image Server niet kan worden gestart.

Start de service Afbeelding opnieuw nadat u dit bestand hebt bewerkt om ervoor te zorgen dat de wijzigingen van kracht worden. Alleen de hieronder gemarkeerde element-/kenmerkwaarden worden ondersteund voor wijziging. Bewerk alleen alle andere inhoud van dit bestand op advies van de technische ondersteuning van Dynamic Media.

```
<supervisor>
    <config>
        <tcpport>9910</tcpport>
        <log>SV::log</log>
        <temp>SV::temp</temp>
        <tracelevel>SV::tracelevel</tracelevel>
        <tracestatsinterval>600</tracestatsinterval>
    </config>
    <servers>
        <server id="is">
            <description>Dynamic Media Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Dynamic Media SVG server</description>
            <profile ref="Java32"/>
            <profile ref="SVG"/>
            <arguments>
                <argument>-XmxSV::SvgHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9998</argument>
            </arguments>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="ps">
            <description>Dynamic Media Platform Server</description>
            <profile ref="Java32"/>
            <profile ref="PlatformServer"/>
            <profile ref="Tomcat"/>
            <arguments>
                <argument>-XmxSV::PsHeapSize</argument>
                <argument>-XX:MaxPermSize=200m</argument>
                <argument>-Dcom.sun.management.jmxremote.port=9999</argument>
            </arguments>
            <startPriority>2</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
    </servers>
</supervisor>
```
