---
description: Image Serving prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité avec SVG 1.1 est requise.
solution: Experience Manager
title: Prise en charge SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# Prise en charge SVG{#svg-support}

Image Serving prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité avec SVG 1.1 est requise.

La diffusion d’images ne reconnaît que les contenus SVG statiques ; Les animations, scripts et autres contenus interactifs ne sont pas pris en charge.

SVG peut être spécifié partout où les fichiers image sont autorisés (chemin d’URL, `src=`et `mask=`). Une fois que le contenu du fichier SVG est pixellisé, il est traité comme une image.

Semblables aux images, les fichiers SVG peuvent être spécifiés en tant qu’entrées de catalogue d’images ou en tant que chemins d’accès relatifs.

## Variables de substitution {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` Les variables de substitution peuvent être incluses dans le fichier SVG dans les chaînes de valeur, les `<text>` éléments et tout attribut d’élément.

Les variables importantes de la partie requête des requêtes de diffusion d’images incorporées ne sont pas substituées directement. Au lieu de cela, toutes les définitions de variables disponibles sont ajoutées à la demande, ce qui permet à Image Serving de substituer des variables lors de l’analyse de la demande.

Voir [Variables](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) de substitution pour plus d’informations.

## Références d’images {#section-a7680f9e6aca4b1a83560637cc9fac66}

Les images peuvent être insérées dans SVG à l’aide de l’élément `<image>` . Les images référencées par l’attribut `xlink::href` de l’élément `<image>` doivent être des requêtes de diffusion d’images valides. Les URL étrangères ne sont pas autorisées.

Spécifiez une demande de diffusion d’images complète, commençant par `http://`, ou une URL relative, commençant par `/is/image`. Si un chemin HTTP complet est spécifié, le nom de domaine est supprimé du chemin à convertir au format relatif. L’utilisation d’un chemin HTTP complet peut être avantageuse, car elle permet de prévisualiser le fichier avec un moteur de rendu SVG tiers.

>[!NOTE]
>
>La prise en charge du rendu des images dans cette version du serveur d’images est limitée. Le référencement d’images à partir de SVG ne doit être utilisé que dans les situations où les mécanismes traditionnels de superposition et de création de modèles du serveur d’images sont insuffisants pour obtenir le résultat souhaité. SVG ne doit en aucun cas être utilisé pour générer des composites multi-images.

>[!NOTE]
>
>Pour l’instant, les images intégrées au format SVG ne sont pas redimensionnées automatiquement. Assurez-vous que tous les href d’image incluent les commandes de diffusion d’images nécessaires pour définir la taille d’image souhaitée (par exemple, `wid=`). Si la taille de l’image n’est pas définie explicitement, `attribute::DefaultPix` est appliqué.

## Gestion des couleurs {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Toutes les valeurs de couleur incorporées dans les fichiers SVG et transmises aux modèles SVG par le biais de variables de substitution sont supposées exister dans l’espace `sRgb` colorimétrique.

Aucune conversion des couleurs n’est effectuée lorsque des images sont incorporées dans le SVG. Pour garantir la fidélité des couleurs, veillez à spécifier `icc=sRgb` toutes les demandes d’image incorporées.

Après la pixellisation, l’image SVG participe à la gestion des couleurs comme toute autre image.

## Exemple {#section-036cdd45abd449849ee00a8f21788c28}

Le modèle SVG suivant illustre les références d’images et l’utilisation de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Ce modèle SVG peut être utilisé comme suit :

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

Les fichiers SVG doivent être autonomes et ne doivent pas référencer de fichiers ou de ressources secondaires, à l’exception des images externes référencées avec Image Serving ou Image Rendering (voir ci-dessus).

Seul le contenu statique est rendu. animation, fonctions interactives telles que les boutons, etc. peut être présente mais ne pas être rendue comme prévu.

Les spécifications de couleur basées sur le profil ICC ne sont pas prises en charge pour le moment.

`<script>` Des éléments peuvent être présents mais sont toujours ignorés.

## Voir aussi {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [spécification SVG 1.1](https://www.w3.org/TR/SVG11/)
