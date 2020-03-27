---
description: Eigenschapsgegevens bestaan uit een tekenreeks die een of meer eigenschappen vertegenwoordigt.
seo-description: Eigenschapsgegevens bestaan uit een tekenreeks die een of meer eigenschappen vertegenwoordigt.
seo-title: Eigenschapsgegevens
solution: Experience Manager
title: Eigenschapsgegevens
topic: Scene7 Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Eigenschapsgegevens{#property-data}

Eigenschapsgegevens bestaan uit een tekenreeks die een of meer eigenschappen vertegenwoordigt.

Een eigenschap bestaat uit een eigenschapnaam en een eigenschapswaarde, gescheiden door =.

Meerdere eigenschappen worden gescheiden door lijnscheidingstekens, die `??` of `<CR><LF>`kunnen zijn. Als de volledige tekenreeks met eigenschapsgegevens niet tussen aanhalingstekens staat, vervangt de server elke instantie van de eigenschap door `??` `<CR><LF>` voordat de gegevens naar de client worden verzonden. Namen van eigenschappen kunnen bestaan uit letters, cijfers, &#39;.&#39;, &#39;-&#39; en &#39;_&#39;. Namen van eigenschappen zijn niet hoofdlettergevoelig.

Eigenschapwaarden mogen geen regelscheidingstekens bevatten.

Zie [Tekstreeks](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) voor aanvullende regels die op Eigenschapgegevens worden toegepast.
