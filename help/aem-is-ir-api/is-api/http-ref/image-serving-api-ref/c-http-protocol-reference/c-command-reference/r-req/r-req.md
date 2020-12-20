---
description: Type de demande. Indique le type de requête.
seo-description: Type de demande. Indique le type de requête.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 9%

---


# req{#req}

Type de demande. Indique le type de requête.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options`*]`

* [catalogprops](r-catalogprops.md)
* [existe](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [carte](r-map-req.md)
* [masque](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [props](r-props.md)
* [résoudre](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [définir](r-set.md)
* [cibles](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [valider](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Sauf indication contraire dans les descriptions détaillées, le serveur renvoie des réponses `text` de type MIME `text/plain`. De nombreux types de requête vous permettent de spécifier un type de réponse, tel que `text`, qui est généralement le type par défaut, `javascript`, `xml` ou `json`. Les types MIME de réponse associés sont `text/plain`, `text/javascript`, `text/xml` et `text/javascript`, respectivement.

Sauf indication contraire, les réponses formatent la réponse sous la forme d&#39;un ensemble de paires `name=value`.

Voir [Propriétés](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
