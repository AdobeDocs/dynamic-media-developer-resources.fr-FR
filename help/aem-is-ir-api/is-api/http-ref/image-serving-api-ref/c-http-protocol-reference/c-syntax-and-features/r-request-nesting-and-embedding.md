---
description: Image Serving prend en charge l’imbrication illimitée de requêtes de diffusion d’images, l’incorporation de requêtes de rendu d’images et l’incorporation d’images récupérées à partir de serveurs étrangers. Seuls les images de calque et les masques de calque prennent en charge ces mécanismes.
seo-description: Image Serving prend en charge l’imbrication illimitée de requêtes de diffusion d’images, l’incorporation de requêtes de rendu d’images et l’incorporation d’images récupérées à partir de serveurs étrangers. Seuls les images de calque et les masques de calque prennent en charge ces mécanismes.
seo-title: Demande d’imbrication et d’incorporation
solution: Experience Manager
title: Demande d’imbrication et d’incorporation
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1089'
ht-degree: 0%

---


# Demande d’imbrication et d’incorporation{#request-nesting-and-embedding}

Image Serving prend en charge l’imbrication illimitée de requêtes de diffusion d’images, l’incorporation de requêtes de rendu d’images et l’incorporation d’images récupérées à partir de serveurs étrangers. Seuls les images de calque et les masques de calque prennent en charge ces mécanismes.

>[!NOTE]
>
>Certains clients de messagerie et serveurs proxy peuvent coder les accolades utilisées pour la syntaxe d’imbrication et d’incorporation. Les applications pour lesquelles il s’agit d’un problème doivent utiliser des parenthèses plutôt que des accolades.

## Requêtes de diffusion d’images imbriquées {#section-6954202119e0466f8ff27c79f4f039c8}

Une requête de diffusion d’images complète peut être utilisée comme source de calque en la spécifiant dans la commande `src=` (ou `mask=`) en utilisant la syntaxe suivante :

`…&src=is( nestedRequest)&…`

Le jeton `is` est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin d’accès racine du serveur (généralement ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En fait, les requêtes imbriquées doivent être codées de la même manière que la requête externe (imbriquée).

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

`attribute::MaxPix`et `attribute::DefaultPix` du catalogue d’images qui s’applique à la demande imbriquée sont également ignorés.

Le résultat d&#39;image d&#39;une requête IS imbriquée peut être mis en cache éventuellement en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre demande dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Demandes de rendu d’image incorporées {#section-69c5548db930412b9b90d9b2951a6969}

Lorsque le rendu des images Dynamic Media est activé sur le serveur, les requêtes de rendu peuvent être utilisées comme sources de calque en les spécifiant dans la commande src= (ou mask=). Utilisez la syntaxe suivante :

` …&src=ir( *[!DNL renderRequest]*)&…`

Le jeton `ir` est sensible à la casse.

*[!DNL renderRequest]* est la requête de rendu d’image habituelle, à l’exception du chemin racine HTTP  ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes de rendu d’image suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Sont également ignorées `attribute::MaxPix` et `attribute::DefaultPix` du catalogue de matières qui s’applique à la demande de rendu imbriquée.

Le résultat d&#39;image d&#39;une requête IR imbriquée peut être mis en cache éventuellement en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre demande dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Demandes de rendu FXG incorporées {#section-c817e4b4f7da414ea5a51252ca7e120a}

Lorsque le rendu graphique FXG (alias [!DNL AGMServer]) est installé et activé avec Image Serving, les requêtes FXG peuvent être utilisées comme sources de calques en les spécifiant dans les commandes `src=` (ou `mask=`). Utilisez la syntaxe suivante :

`…&src=fxg( renderRequest)&…`

Le jeton `fxg` est sensible à la casse.

>[!NOTE]
>
>Le rendu des graphiques FXG n’est disponible que dans l’environnement hébergé par Dynamic Media et peut nécessiter une licence supplémentaire. Contactez l’assistance technique de Dynamic Media pour plus d’informations.

*[!DNL renderRequest]* est la requête de rendu FXG habituelle, à l’exception du chemin d’accès racine HTTP  ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Les caractères de délimiteur ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes FXG suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Sources d’images étrangères {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Serving prend en charge l’accès aux images source sur les serveurs HTTP étrangers.

>[!NOTE]
>
>Seul le protocole HTTP est pris en charge pour les URL distantes.

Pour spécifier une URL étrangère pour une commande `src=` ou `mask=`, délimitez l’URL étrangère ou le fragment d’URL entre parenthèses :

`…&src=( foreignUrl)&…`

Important Les caractères de délimiteur ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les URL absolues complètes (si `attribute::AllowDirectUrls` est défini) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et que l’attribut : `AllowDirectUrls` est 0 ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Bien que les URL étrangères ne puissent pas être spécifiées directement dans le composant de chemin d’accès de l’URL de requête, il est possible de configurer une règle de prétraitement pour permettre la conversion des chemins relatifs en URL absolues (voir l’exemple ci-dessous).

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP. Si aucun en-tête de réponse HTTP `ETag` ou Last-Modified n’est présent, la réponse n’est pas mise en cache. Cela peut entraîner des performances médiocres pour les accès répétés pour la même image étrangère, car la diffusion d’images doit récupérer et revalider l’image à chaque accès.

Ce mécanisme prend en charge les mêmes formats de fichier d’image que ceux pris en charge par l’utilitaire de conversion d’image (IC), à l’exception des images source avec 16 bits par composant.

>[!NOTE]
>
>La diffusion d’images exécute automatiquement l’utilitaire de validation lorsqu’une image étrangère est utilisée pour la première fois, afin de s’assurer que l’image est valide et n’a pas été endommagée pendant la transmission. Ceci peut provoquer un léger retard sur le premier accès. Pour de meilleures performances, il est recommandé de limiter la taille de ces images et/ou d’utiliser un format de fichier image qui se compresse bien.

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

La taille de l’image générée par des requêtes imbriquées/incorporées est généralement automatiquement optimisée. Si la mise en cache des images de requête imbriquée est activée, des gains de performances incrémentiels peuvent être obtenus en spécifiant la taille exacte de l’image imbriquée, de sorte qu’aucune mise à l’échelle supplémentaire n’est requise lorsque l’entrée de cache est réutilisée.

Important Image Serving ne prend pas en charge le codage par doublon des requêtes imbriquées ou incorporées. Les requêtes imbriquées et incorporées doivent être codées en HTTP, tout comme les requêtes simples.

## Exemples {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modèle de mise en page avec mise en cache :**

Utilisez l’imbrication pour ajouter la mise en cache à un modèle de mise en calque. Un nombre limité d’images d’arrière-plan sont superposées avec du texte très variable. La chaîne de modèle initiale peut se présenter comme suit :

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Avec de légères modifications, nous pouvons pré-dimensionner l’image du calque 0 et la mettre en cache de façon permanente, réduisant ainsi la charge du serveur :

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporation de requêtes pour le rendu des images Dynamic Media**

Utilisation d&#39;un modèle stocké dans [!DNL myCatalog/myTemplate]; générez l’image pour le calque2 du modèle à l’aide du rendu d’image Dynamic Media :

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Notez les accolades imbriquées. La demande de rendu d’image incorpore un appel à Image Serving pour récupérer une texture répétable.

## Voir aussi {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference,  [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)[
