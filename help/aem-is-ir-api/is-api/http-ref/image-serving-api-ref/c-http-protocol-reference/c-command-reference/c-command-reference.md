---
description: In deze sectie worden de HTTP-protocolopdrachten beschreven.
seo-description: In deze sectie worden de HTTP-protocolopdrachten beschreven.
seo-title: Opdrachtverwijzing
solution: Experience Manager
title: Opdrachtverwijzing
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f

---


# Opdrachtverwijzing{#command-reference}

In deze sectie worden de HTTP-protocolopdrachten beschreven.

**Alleen** voor dynamische media in AEM: Naast de basisafbeeldingsinstellingen die beschikbaar zijn in de gebruikersinterface, ondersteunt [!DNL Dynamic Media] AEM ( [!DNL Adobe Experience Manager]) tal van geavanceerde afbeeldingswijzigingen die u kunt opgeven in het veld **Afbeeldingswijzigingstoetsen** . Deze parameters worden hieronder gedefinieerd. Houd er echter rekening mee dat de volgende functionaliteit niet wordt ondersteund in Dynamic Media in AEM.

* Opdrachten voor kleurcorrectie: `icc=` en `iccEmbed=`.
* Standaardopdrachten voor sjablonen en tekstrendering: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` en `textPs=`.
* Localisatie-opdrachten: `locale=` en `req=xlate`.
* `req=set` is niet beschikbaar voor algemeen gebruik.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Niet-kernservices voor dynamische media: SVG, Afbeelding renderen en Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Zie ook de Dynamische [Vooraf ingestelde Opties](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options) van het Beeld van Media in de documentatie AEM 6.5.

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
