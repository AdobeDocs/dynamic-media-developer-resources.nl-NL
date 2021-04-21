---
description: Eigenschapsgegevens bestaan uit een tekenreeks die een of meer eigenschappen vertegenwoordigt.
solution: Experience Manager
title: Eigenschapsgegevens
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Eigenschapsgegevens{#property-data}

Eigenschapsgegevens bestaan uit een tekenreeks die een of meer eigenschappen vertegenwoordigt.

Een eigenschap bestaat uit een eigenschapnaam en een eigenschapswaarde, gescheiden door =.

Meerdere eigenschappen worden gescheiden door lijnscheidingstekens, die `??` of `<CR><LF>` kunnen zijn. Als de volledige tekenreeks met eigenschapsgegevens niet tussen aanhalingstekens staat, vervangt de server elk exemplaar van `??` door `<CR><LF>` voordat de gegevens naar de client worden verzonden. Namen van eigenschappen kunnen bestaan uit letters, cijfers, &#39;.&#39;, &#39;-&#39; en &#39;_&#39;. Namen van eigenschappen zijn niet hoofdlettergevoelig.

Eigenschapwaarden mogen geen regelscheidingstekens bevatten.

Zie [Tekstreeks](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) voor extra regels die worden toegepast op Eigenschapsgegevens.
