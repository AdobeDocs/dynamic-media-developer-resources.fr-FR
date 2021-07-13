---
description: Métadonnées XMP. Renvoie les métadonnées XMP associées à l’image spécifiée dans le chemin d’accès de la requête.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 12%

---

# xmp{#xmp}

Métadonnées XMP. Renvoie les métadonnées XMP associées à l’image spécifiée dans le chemin d’accès de la requête.

`req=xmp`

Les autres commandes sont ignorées. Le codage UTF-8 s’applique. La réponse est formatée au format XML avec le type MIME `text/xml`.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

## Propriétés {#section-0d26b6a56c844153ae5cea4880370d00}

Attribut de requête. S’applique quel que soit le paramètre de calque actif.

## Par défaut {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Si l’URL ne contient pas de chemin d’image ou de modificateurs, alors :

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

Sinon, `req=img`

## Exemples {#section-34213692deab4a0f9037d5844132ee14}

Requête sur les propriétés du fichier image.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Propriétés du catalogue d’images de requête :

` http:// *`server`*/myRootId?req=catalogprops`

Accédez aux propriétés d’une entrée de catalogue d’images à partir d’un script JavaScript côté client incorporé dans un fichier HTML :

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Récupérez l’image de masque pour une entrée de catalogue spécifique, mise à l’échelle à 25 % de la taille d’origine :

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Demandez une image à une taille d’un huitième :

` http:// *`server`*/myRootId/myImageId?scl=8`

Il s’agit de la même chose que :

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Demandez une miniature d’une image en fonction des attributs de miniature spécifiés dans le catalogue d’images :

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Envoyez un message texte aux logs du serveur :

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Voir aussi {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [catalogue::Cibles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [catalogue::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md),  [mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f),  [propriétés](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9),  [zones cliquables](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
