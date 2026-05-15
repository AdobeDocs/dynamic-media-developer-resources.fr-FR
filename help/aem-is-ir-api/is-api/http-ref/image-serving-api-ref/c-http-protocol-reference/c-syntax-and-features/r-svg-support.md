---
description: La diffusion d’images prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité à SVG 1.1 est requise.
solution: Experience Manager
title: Prise en charge de SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 60e40195-710f-4f03-b152-52eaa10c5b21
TQID: 'https://experienceleague.adobe.com/yN93vSajgH09FJqxpDsa1j3fFlBR9EdCREXvhUy8q2U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 514
ht-degree: 0%

---

# Prise en charge de SVG{#svg-support}

La diffusion d’images prend en charge les fichiers SVG (Scalable Vector Graphics) en tant que données source. La conformité à SVG 1.1 est requise.

La diffusion d’images reconnaît uniquement les contenus SVG statiques. Les animations, les scripts et autres contenus interactifs ne sont pas pris en charge.

SVG peut être spécifié là où les fichiers image sont autorisés (chemin URL, `src=` et `mask=`). Une fois le contenu du fichier SVG pixellisé, il est géré comme une image.

Tout comme pour les images, les fichiers SVG peuvent être spécifiés en tant qu’entrées de catalogue d’images ou en tant que chemins d’accès aux fichiers relatifs.

## Variables de substitution {#section-83b149f13f244193901df39b204c975b}

` $ *[!DNL var]*$` variables de substitution peuvent être incluses dans le fichier SVG dans les chaînes de valeurs `<text>` les éléments et tout attribut d’élément.

Les variables importantes dans la partie requête des requêtes de diffusion d’images incorporées ne sont pas remplacées directement. Au lieu de cela, toutes les définitions de variable disponibles sont ajoutées à la requête, ce qui permet au service d’images de substituer des variables lors de l’analyse de la requête.

Voir [Variables de substitution](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a) pour plus d’informations.

## Références d’image {#section-a7680f9e6aca4b1a83560637cc9fac66}

Les images peuvent être insérées dans SVG à l’aide de l’élément `<image>`. Les images référencées par l’attribut `xlink::href` de l’élément `<image>` doivent être des requêtes de diffusion d’images valides. Les URL étrangères ne sont pas autorisées.

Spécifiez soit une requête de diffusion d’images complète, commençant par `http://`, soit une URL relative, commençant par `/is/image`. Si un chemin HTTP complet est spécifié, le nom de domaine est supprimé du chemin pour être converti au format relatif. L’utilisation d’un chemin d’accès HTTP complet peut s’avérer avantageuse, car elle permet de prévisualiser le fichier avec un moteur de rendu SVG tiers.

>[!NOTE]
>
>La prise en charge du rendu des images dans cette version de la diffusion d’images est limitée. Le référencement d’images depuis SVG ne doit être utilisé que dans les cas où les mécanismes de superposition et de création de modèles de diffusion d’images traditionnels sont insuffisants pour obtenir le résultat souhaité. SVG ne doit en aucun cas être utilisé pour générer des composites à plusieurs images.

>[!NOTE]
>
>Les images incorporées dans SVG ne sont pas redimensionnées automatiquement pour le moment. Veillez à ce que tous les arborescences d’images incluent les commandes de diffusion d’images nécessaires pour définir la taille d’image souhaitée (par exemple, `wid=`). Si la taille de l’image n’est pas définie explicitement, la `attribute::DefaultPix` est appliquée.

## Gestion des couleurs {#section-ea76e2bc4e1842638aa97a2d470c8a68}

Toutes les valeurs de couleur incorporées dans des fichiers SVG et transmises aux modèles SVG par le biais de variables de substitution sont supposées exister dans l’espace colorimétrique `sRgb`.

Aucune conversion de couleurs n’est effectuée lorsque des images sont incorporées dans le SVG. Pour garantir la fidélité des couleurs, veillez à spécifier `icc=sRgb` pour toutes les demandes d’images incorporées.

Après la pixellisation, l’image SVG participe à la gestion des couleurs comme toute autre image.

## Exemple {#section-036cdd45abd449849ee00a8f21788c28}

Le modèle SVG suivant illustre les références d’image et l’utilisation de variables.

`<?xml version="1.0" standalone="no"?> <!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 20010904//EN" "http://www.w3.org/TR/2001/REC-SVG-20010904/DTD/svg10.dtd"> <svg width="500" height="500"> <image x="50" y="50" width="400" height="400" xlink:href="/is/image?src=$img$&wid=300&hei=400"/> <text x="150" y="400" style="font-size:$pts$; fill:$color$"> Title: $txt$ </text> </svg>`

Ce modèle SVG peut être utilisé comme suit :

`http://server/is/image/mySvgTemplate.svg?$txt=Svg%20Template%20Test&$img=myImage.tif&$color=red&$pts=40&qlt=95`

## Restrictions {#section-daa5eccd07204aaf993be41e87822d54}

Les fichiers SVG doivent être autonomes et ne doivent pas référencer de fichiers ou de ressources secondaires, à l’exception des images externes référencées avec des demandes de diffusion d’images ou de rendu d’images (voir ci-dessus).

Seul le contenu statique est rendu. Animation, fonctions interactives, telles que des boutons, etc. peut être présent mais peut ne pas être rendu comme prévu.

Les spécifications de couleurs basées sur les profils ICC ne sont pas prises en charge pour le moment.

`<script>` éléments peuvent être présents mais sont toujours ignorés.

## Voir aussi {#section-901dd1775fd24154a766dcfbe5032b67}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Spécification de SVG 1.1](https://www.w3.org/TR/SVG11/)
