---
description: Type de requête. Spécifie le type de demande.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
TQID: 'https://experienceleague.adobe.com/-WzHmELeamQBbVFlzXNKbDE3fKVXw4x6pSoEz0LHav4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 8%

---

# req{#req}

Type de requête. Spécifie le type de demande.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`options `*]`

* [catalogprops](r-catalogprops.md)
* [existe](r-exists.md)
* [imageprops](r-imageprops.md)
* [visionneuse d’images](r-imageset-req.md)
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
* [œillet](r-tmb.md)
* [userdata](r-userdata.md)
* [valider](r-is-http-validate.md)
* [ardoise](r-xlate.md)
* [xmp](r-xmp.md)

Sauf indication contraire dans les descriptions détaillées, le serveur renvoie des réponses `text` avec le type MIME `text/plain`. De nombreux types de requête vous permettent de spécifier un type de réponse, tel que `text` qui est généralement la valeur par défaut, `javascript`, `xml` ou `json`. Les types MIME de réponse associés sont `text/plain`, `text/javascript`, `text/xml` et `text/javascript`, respectivement.

Sauf indication contraire, les réponses mettent en forme la réponse sous la forme d’un ensemble de paires de `name=value`.

Voir [Propriétés](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
