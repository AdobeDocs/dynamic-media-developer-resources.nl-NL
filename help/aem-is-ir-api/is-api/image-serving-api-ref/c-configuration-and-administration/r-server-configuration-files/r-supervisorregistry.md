---
description: Bevat configuratie-instellingen voor servertoezicht.
seo-description: Bevat configuratie-instellingen voor servertoezicht.
seo-title: SupervisorRegistry.xml
solution: Experience Manager
title: SupervisorRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 8442a3d6-5f45-48d1-8e6e-71f0ed384227
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# SupervisorRegistry.xml{#supervisorregistry-xml}

Bevat configuratie-instellingen voor servertoezicht.

Zorg dat u bij het bewerken van dit XML-bestand een geldige XML-syntaxis behoudt, anders kan het zijn dat de Image Server niet kan worden gestart.

Start de service Afbeelding opnieuw nadat u dit bestand hebt bewerkt om ervoor te zorgen dat de wijzigingen van kracht worden. Alleen de hieronder gemarkeerde element-/kenmerkwaarden worden ondersteund voor wijziging. Bewerk alleen alle andere inhoud van dit bestand op advies van Scene7 Technical Support.

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
            <description>Scene7 Image Server</description>
            <profile ref="SV::ImageServerMode"/>
            <startPriority>1</startPriority>
            <startDelay>5</startDelay>
            <stopTimeout>60</stopTimeout>
        </server>
        <server id="svg">
            <description>Scene7 SVG server</description>
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
            <description>Scene7 Platform Server</description>
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

