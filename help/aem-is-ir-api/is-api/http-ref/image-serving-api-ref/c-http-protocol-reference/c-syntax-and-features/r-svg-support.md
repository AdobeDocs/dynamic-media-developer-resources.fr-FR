---
description: La diffusion d’images prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité avec SVG 1.1 est requise.
solution: Experience Manager
title: Prise en charge de SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Prise en charge de SVG{#svg-support}

La diffusion d’images prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité avec SVG 1.1 est requise.

Image Serving reconnaît uniquement le contenu statique des fichiers SVG ; les animations, les scripts et autres contenus interactifs ne sont pas pris en charge.

SVG peut être spécifié partout où les fichiers d’image sont autorisés (chemin d’accès à l’URL, `src=` et `mask=`). Une fois le contenu du fichier SVG pixellisé, il est géré comme une image.

Comme pour les images, les fichiers SVG peuvent être spécifiés en tant qu’entrées de catalogue d’images ou en tant que chemins d’accès aux fichiers relatifs.

## Variables de substitution {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` les variables de substitution peuvent être incluses dans le fichier SVG dans les  `<text>` éléments de chaînes de valeur et tout attribut d’élément.

Les variables importantes figurant dans la partie requête des demandes de diffusion d’images incorporées ne sont pas directement remplacées. En revanche, toutes les définitions de variable disponibles sont ajoutées à la requête, ce qui permet à Image Serving de remplacer les variables lors de l’analyse de la requête.

Voir [Variables de substitution](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) pour plus d&#39;informations.

## Références d&#39;image {#section-a7680f9e6aca4b1a83560637cc9fac66}

Les images peuvent être insérées dans SVG à l’aide de l’élément `<image>`. Les images référencées par l&#39;attribut `xlink::href` de l&#39;élément `<image>` doivent être des demandes de diffusion d&#39;images valides. Les URL étrangères ne sont pas autorisées.

Spécifiez soit une requête de diffusion d’images complète, commençant par `http://`, soit une URL relative, commençant par `/is/image`. Si un chemin HTTP complet est spécifié, le nom de domaine est supprimé du chemin pour être converti au format relatif. L’utilisation d’un chemin HTTP complet peut s’avérer utile, car elle permet de prévisualiser le fichier avec un rendu SVG tiers.

>[!NOTE]
>
>La prise en charge du rendu des images dans cette version d’Image Serving est limitée. Le référencement d’images à partir de SVG ne doit être utilisé que dans les situations où les mécanismes de calage et de modélisation traditionnels de la diffusion d’images sont insuffisants pour obtenir le résultat souhaité. En aucun cas, SVG ne doit être utilisé pour générer des composites à plusieurs images.

>[!NOTE]
>
>Actuellement, les images incorporées dans SVG ne sont pas redimensionnées automatiquement. Assurez-vous que toutes les références d’image comportent les commandes de diffusion d’images nécessaires pour définir la taille d’image souhaitée (ex. `wid=`). Si la taille de l’image n’est pas définie explicitement, `attribute::DefaultPix` est appliqué.

## Gestion des couleurs {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Toutes les valeurs de couleur incorporées dans les fichiers SVG et transmises aux modèles SVG par le biais de variables de substitution sont supposées exister dans l’espace colorimétrique `sRgb`.

Aucune conversion de couleur n’est effectuée lorsque des images sont incorporées au fichier SVG. Pour garantir la fidélité des couleurs, veillez à spécifier `icc=sRgb` pour toutes les demandes d’image incorporées.

Après la pixellisation, l’image SVG participe à la gestion des couleurs comme toute autre image.

## Exemple {#section-036cdd45abd449849ee00a8f21788c28}

Le modèle SVG suivant illustre les références d’image et l’utilisation de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Ce modèle SVG peut être utilisé comme suit :

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

Les fichiers SVG doivent être autonomes et ne doivent pas référencer de fichiers ou de ressources secondaires, à l’exception des images externes référencées avec les demandes de diffusion d’images ou de rendu d’images (voir ci-dessus).

Seul le contenu statique est rendu. Animation, fonctions interactives, telles que boutons, etc. peut être présent mais ne pas être rendu comme prévu.

Actuellement, les spécifications de couleur basées sur un profil ICC ne sont pas prises en charge.

`<script>` peuvent être présents mais sont toujours ignorés.

## Voir aussi {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [SVG 1.1 Spécifications](http://www.w3.org/TR/SVG11/)
