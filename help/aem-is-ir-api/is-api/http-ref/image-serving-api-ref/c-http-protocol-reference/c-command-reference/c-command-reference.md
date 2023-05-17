---
title: Opdrachtverwijzing
description: In deze sectie worden de HTTP-protocolopdrachten beschreven.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 187de979d7d1f7ce92b7b4c8b7661a787ab6889f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Opdrachtverwijzing{#command-reference}

In deze sectie worden de HTTP-protocolopdrachten beschreven.

>[!TIP]
>
>Uitproberen en ontdekken wat de voordelen zijn van Dynamic Media-beeldmodifiers en Smart Imaging met Dynamic Media [_Opname_](https://snapshot.scene7.com/).
>
> Momentopname is een visueel demonstratieprogramma dat is ontworpen om de kracht van Dynamic Media te illustreren voor geoptimaliseerde en dynamische beeldlevering. Experimenteer met testafbeeldingen of Dynamic Media-URL&#39;s om visueel de uitvoer van verschillende Dynamic Media-afbeeldingsmodifiers en Smart Imaging-optimalisaties te bekijken voor:
>* Bestandsgrootte (met WebP en AVIF levering)
>* Netwerkbandbreedte
>* DPR (pixelverhouding apparaat)
>
>Als u wilt weten hoe eenvoudig het is om Momentopname te gebruiken, speelt u de opdracht [Video over momentopnamen](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) (3 minuten en 17 seconden).


**Alleen voor Dynamic Media in Adobe Experience Manager** - Buiten de basisafbeeldingsinstellingen die beschikbaar zijn in de gebruikersinterface, [!DNL Dynamic Media] in AEM ( [!DNL Adobe Experience Manager]) ondersteunt talrijke geavanceerde afbeeldingswijzigingen die u kunt opgeven in het dialoogvenster **Afbeeldingsaanpassingen** veld. Deze parameters worden hieronder gedefinieerd. Houd er echter rekening mee dat de volgende functionaliteit niet in Dynamic Media in AEM wordt ondersteund.

* Opdrachten voor kleurcorrectie: `icc=` en `iccEmbed=`.
* Standaardopdrachten voor sjablonen en tekstrendering: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` en `textPs=`.
* Localisatie-opdrachten: `locale=` en `req=xlate`.
* `req=set` is niet beschikbaar voor algemeen gebruik.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Niet-kernservices van Dynamic Media: SVG, Afbeelding renderen en Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Zie ook de Dynamic Media [Opties voorinstelling afbeelding](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) in de documentatie AEM 6.5.

* [align](r-align.md)
* [anker](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cachegeheugen](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [kleur](r-color-commandref.md)
* [uitsnijden](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [effect](r-effect.md)
* [effectMask](r-effectmask.md)
* [uitbreiden](r-extend.md)
* [aanpassen](r-fit.md)
* [omdraaien](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [verbergen](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [laag](r-layer.md)
* [landinstelling](r-locale.md)
* [map](r-map.md)
* [masker](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_vervagen](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_kleurbalans](r-op-colorbalance.md)
* [op_inkleuren](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_kweken](r-op-grow.md)
* [op_kwekenMasker](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_ruis](r-op-noise.md)
* [op_verzadiging](r-op-saturation.md)
* [op_scherpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [oorsprong](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [perspectief](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [kwantificeren](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [roteren](r-rotate.md)
* [schalen](r-is-http-scale.md)
* [scl](r-scl.md)
* [size](r-size-reference.md)
* [src](r-src.md)
* [template](r-template.md)
* [text](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [winderig](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
