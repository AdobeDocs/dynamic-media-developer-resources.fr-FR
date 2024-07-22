---
description: Type de requête. Indique le type de requête.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# req{#req}

Type de requête. Indique le type de requête.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options`*]`

* [catalogprops](r-catalogprops.md)
* [existe](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [carte](r-map-req.md)
* [mask](r-mask-req.md)
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

Sauf indication contraire dans les descriptions détaillées, le serveur renvoie des réponses `text` avec le type MIME `text/plain`. De nombreux types de requête vous permettent de spécifier un type de réponse, tel que `text` qui est généralement le type par défaut, `javascript`, `xml` ou `json`. Les types MIME de réponse associés sont `text/plain`, `text/javascript`, `text/xml` et `text/javascript`, respectivement.

Sauf indication contraire, les réponses formatent la réponse sous la forme d’un ensemble de paires `name=value`.

Voir [Propriétés](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
