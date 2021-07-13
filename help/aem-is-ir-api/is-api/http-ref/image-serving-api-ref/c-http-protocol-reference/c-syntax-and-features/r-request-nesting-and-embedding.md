---
description: Le service d’images prend en charge l’imbrication illimitée de demandes de diffusion d’images, l’incorporation de demandes de rendu d’images et l’incorporation d’images récupérées à partir de serveurs étrangers. Seules les images de calque et les masques de calque prennent en charge ces mécanismes.
solution: Experience Manager
title: Demande d’imbrication et d’incorporation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# Demande d’imbrication et d’incorporation{#request-nesting-and-embedding}

Le service d’images prend en charge l’imbrication illimitée de demandes de diffusion d’images, l’incorporation de demandes de rendu d’images et l’incorporation d’images récupérées à partir de serveurs étrangers. Seules les images de calque et les masques de calque prennent en charge ces mécanismes.

>[!NOTE]
>
>Certains clients de messagerie et serveurs proxy peuvent coder les accolades utilisées pour la syntaxe d’imbrication et d’incorporation. Les applications pour lesquelles il s’agit d’un problème doivent utiliser des parenthèses plutôt que des accolades.

## Demandes de diffusion d’images imbriquées {#section-6954202119e0466f8ff27c79f4f039c8}

Une requête de diffusion d’images entière peut être utilisée comme source de calque en la spécifiant dans la commande `src=` (ou `mask=`) à l’aide de la syntaxe suivante :

`…&src=is( nestedRequest)&…`

Le jeton `is` est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin racine du serveur (généralement ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En fait, les requêtes imbriquées doivent être codées de la même manière que la requête externe (imbrication).

Les règles de prétraitement sont appliquées aux requêtes imbriquées.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (soit dans l’URL de la requête, soit dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Si l’image de résultat des requêtes imbriquées inclut des données de masque (alpha), elle est transmise au calque d’incorporation en tant que masque de calque.

`attribute::MaxPix`et `attribute::DefaultPix` du catalogue d’images qui s’applique à la requête imbriquée sont également ignorés.

Le résultat de l’image d’une requête IS imbriquée peut être mis en cache de manière facultative en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Demandes de rendu d’image incorporées {#section-69c5548db930412b9b90d9b2951a6969}

Lorsque le rendu d’image Dynamic Media est activé sur le serveur, les demandes de rendu peuvent être utilisées comme sources de calque en les spécifiant dans la commande src= (ou mask=). Utilisez la syntaxe suivante :

` …&src=ir( *[!DNL renderRequest]*)&…`

Le jeton `ir` est sensible à la casse.

*[!DNL renderRequest]* est la requête de rendu d’image habituelle, à l’exception du chemin racine HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En fait, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes de rendu d’image suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

`attribute::MaxPix` et `attribute::DefaultPix` du catalogue de matières qui s’applique à la demande de rendu imbriquée sont également ignorés.

Le résultat de l’image d’une requête IR imbriquée peut être mis en cache de manière facultative en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Demandes de rendu FXG incorporées {#section-c817e4b4f7da414ea5a51252ca7e120a}

Lorsque le moteur de rendu d’images FXG (alias [!DNL AGMServer]) est installé et activé avec le serveur d’images, les demandes FXG peuvent être utilisées comme sources de calque en les spécifiant dans les commandes `src=` (ou `mask=`). Utilisez la syntaxe suivante :

`…&src=fxg( renderRequest)&…`

Le jeton `fxg` est sensible à la casse.

>[!NOTE]
>
>Le rendu des graphiques FXG est disponible uniquement dans l’environnement hébergé de Dynamic Media et peut nécessiter des licences supplémentaires. Pour plus d’informations, contactez l’assistance technique de Dynamic Media.

*[!DNL renderRequest]* est la requête de rendu FXG habituelle, à l’exception du chemin racine HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Les caractères de délimiteur ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En fait, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes FXG suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Sources d’image étrangères {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Le serveur d’images prend en charge l’accès aux images sources sur les serveurs HTTP étrangers.

>[!NOTE]
>
>Seul le protocole HTTP est pris en charge pour les URL distantes.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=`, délimitez l’URL ou le fragment d’URL étranger par des parenthèses :

`…&src=( foreignUrl)&…`

Important Les caractères de délimiteur ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être codés en HTTP. En fait, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et un attribut : `AllowDirectUrls` correspond à 0 ou si une URL relative est spécifiée et que `attribute::RootUrl` est vide.

Bien que les URL étrangères ne puissent pas être spécifiées directement dans le composant de chemin de l’URL de requête, il est possible de configurer une règle de prétraitement pour permettre la conversion des chemins relatifs en URL absolues (voir l’exemple ci-dessous).

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP. Si aucun en-tête de réponse HTTP `ETag` ou Last-Modified n’est présent, la réponse n’est pas mise en cache. Cela peut entraîner des performances médiocres pour les accès répétés pour la même image étrangère, car le service d’images doit récupérer et revalider l’image à chaque accès.

Ce mécanisme prend en charge les mêmes formats de fichiers image pris en charge par l’utilitaire de conversion d’images (IC), à l’exception des images source avec 16 bits par composant.

>[!NOTE]
>
>La diffusion d’images exécute automatiquement l’utilitaire de validation lorsqu’une image étrangère est utilisée pour la première fois, afin de s’assurer que l’image est valide et n’a pas été corrompue pendant la transmission. Cela peut entraîner un léger retard lors du premier accès. Pour de meilleures performances, il est recommandé de limiter la taille de ces images et/ou d’utiliser un format de fichier image qui se compresse correctement.

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

La taille de l’image générée par les requêtes imbriquées/incorporées est normalement optimisée automatiquement. Si la mise en cache des images de requête imbriquées est activée, des gains de performances incrémentiels peuvent être réalisés en spécifiant la taille exacte de l’image imbriquée, de sorte qu’aucune mise à l’échelle supplémentaire n’est requise lors de la réutilisation de l’entrée de cache.

Important : La diffusion d’images ne prend pas en charge le double codage des requêtes imbriquées ou incorporées. Les requêtes imbriquées et incorporées doivent être codées au format HTTP de la même manière que les requêtes simples.

## Exemples {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modèle de mise en page avec mise en cache :**

Utilisez l’imbrication pour ajouter la mise en cache à un modèle de calque. Un nombre limité d’images d’arrière-plan sont superposées avec du texte très variable. La chaîne de modèle initiale peut se présenter comme suit :

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Avec de légères modifications, nous pouvons pré-dimensionner l’image du calque 0 et la mettre en cache de manière permanente, ce qui réduit la charge du serveur :

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporation de requêtes pour le rendu d’image Dynamic Media**

Utiliser un modèle stocké dans [!DNL myCatalog/myTemplate]; générez l’image pour le calque2 du modèle à l’aide du rendu d’image Dynamic Media :

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Notez les accolades imbriquées. La requête de rendu d’image incorpore un appel vers le serveur d’images pour récupérer une texture répétable.

## Voir aussi {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Request Pre-Processing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference,  [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
