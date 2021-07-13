---
description: La diffusion d’images prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité avec SVG 1.1 est requise.
solution: Experience Manager
title: Prise en charge SVG
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Prise en charge SVG{#svg-support}

La diffusion d’images prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité avec SVG 1.1 est requise.

La diffusion d’images ne reconnaît que les contenus SVG statiques ; les animations, les scripts et autres contenus interactifs ne sont pas pris en charge.

Le format SVG peut être spécifié partout où les fichiers image sont autorisés (chemin URL, `src=` et `mask=`). Une fois le contenu du fichier SVG pixellisé, il est géré comme une image.

Comme pour les images, les fichiers SVG peuvent être spécifiés sous la forme d’entrées de catalogue d’images ou de chemins d’accès aux fichiers relatifs.

## Variables de substitution {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` les variables de substitution peuvent être incluses dans le fichier SVG dans les  `<text>` éléments de chaînes de valeur et tout attribut d’élément.

Les variables importantes de la partie requête des demandes de diffusion d’images incorporées ne sont pas directement remplacées. À la place, toutes les définitions de variable disponibles sont ajoutées à la requête, ce qui permet au serveur d’images de remplacer des variables lors de l’analyse de la requête.

Voir [Variables de substitution](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) pour plus d’informations.

## Références d’image {#section-a7680f9e6aca4b1a83560637cc9fac66}

Les images peuvent être insérées dans SVG à l&#39;aide de l&#39;élément `<image>`. Les images référencées par l’attribut `xlink::href` de l’élément `<image>` doivent être des demandes de diffusion d’images valides. Les URL étrangères ne sont pas autorisées.

Spécifiez une requête de diffusion d’images complète, commençant par `http://`, ou une URL relative, commençant par `/is/image`. Si un chemin HTTP complet est spécifié, le nom de domaine est supprimé du chemin pour être converti au format relatif. L’utilisation d’un chemin HTTP complet peut être un avantage, car elle permet de prévisualiser le fichier avec un moteur de rendu SVG tiers.

>[!NOTE]
>
>La prise en charge du rendu des images dans cette version du serveur d’images est limitée. Le référencement d’images à partir de SVG ne doit être utilisé que dans les cas où les mécanismes traditionnels de calquage et de création de modèles de diffusion d’images ne suffisent pas pour obtenir le résultat souhaité. En aucun cas, SVG ne doit être utilisé pour générer des composites multi-images.

>[!NOTE]
>
>Les images incorporées dans SVG ne sont pas automatiquement redimensionnées pour le moment. Assurez-vous que tous les références d’image incluent les commandes de diffusion d’images nécessaires pour définir la taille d’image souhaitée (par exemple, `wid=`). Si la taille de l’image n’est pas définie explicitement, `attribute::DefaultPix` est appliqué.

## Gestion des couleurs {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Toutes les valeurs de couleur incorporées dans les fichiers SVG et transmises aux modèles SVG via des variables de substitution sont supposées exister dans l’espace colorimétrique `sRgb`.

Aucune conversion de couleur n’est effectuée lorsque les images sont incorporées dans le SVG. Pour garantir la fidélité des couleurs, veillez à spécifier `icc=sRgb` pour toutes les demandes d’image incorporées.

Après pixellisation, l’image SVG participe à la gestion des couleurs comme toute autre image.

## Exemple {#section-036cdd45abd449849ee00a8f21788c28}

Le modèle SVG suivant illustre les références d’image et l’utilisation de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Ce modèle SVG peut être utilisé comme suit :

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

Les fichiers SVG doivent être autonomes et ne doivent pas référencer de fichiers ou de ressources secondaires, à l’exception des images externes référencées avec les demandes de diffusion d’images ou de rendu d’images (voir ci-dessus).

Seul le contenu statique est rendu. Animation, fonctions interactives, telles que des boutons, etc. peut être présent, mais peut ne pas être rendu comme prévu.

Les spécifications de couleur basées sur un profil ICC ne sont pas prises en charge pour le moment.

`<script>` peuvent être présents, mais ils sont toujours ignorés.

## Voir aussi {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [SVG 1.1 Specification](http://www.w3.org/TR/SVG11/)
