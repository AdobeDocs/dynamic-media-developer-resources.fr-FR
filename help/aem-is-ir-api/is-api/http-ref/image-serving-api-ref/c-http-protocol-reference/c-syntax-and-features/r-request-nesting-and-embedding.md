---
description: Image Serving prend en charge l’imbrication illimitée des demandes de diffusion d’images, l’incorporation des demandes de rendu d’images et l’incorporation des images extraites des serveurs étrangers. Seuls les images de calque et les masques de calque prennent en charge ces mécanismes.
seo-description: Image Serving prend en charge l’imbrication illimitée des demandes de diffusion d’images, l’incorporation des demandes de rendu d’images et l’incorporation des images extraites des serveurs étrangers. Seuls les images de calque et les masques de calque prennent en charge ces mécanismes.
seo-title: Imbrication et incorporation des requêtes
solution: Experience Manager
title: Imbrication et incorporation des requêtes
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Imbrication et incorporation des requêtes{#request-nesting-and-embedding}

Image Serving prend en charge l’imbrication illimitée des demandes de diffusion d’images, l’incorporation des demandes de rendu d’images et l’incorporation des images extraites des serveurs étrangers. Seuls les images de calque et les masques de calque prennent en charge ces mécanismes.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Certains clients de messagerie et serveurs proxy peuvent coder les accolades utilisées pour la syntaxe d’imbrication et d’incorporation. Les applications pour lesquelles il s’agit d’un problème doivent utiliser des parenthèses plutôt que des accolades.

## Requêtes de diffusion d’images imbriquées {#section-6954202119e0466f8ff27c79f4f039c8}

Une requête de diffusion d’images entière peut être utilisée comme source de calque en la spécifiant dans la commande `src=` (ou `mask=`) à l’aide de la syntaxe suivante :

`…&src=is( nestedRequest)&…`

Le `is` jeton est sensible à la casse.

La requête imbriquée ne doit pas inclure le chemin racine du serveur (généralement ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En effet, les requêtes imbriquées doivent être codées de la même manière que la requête externe (imbrication).

Les règles de prétraitement sont appliquées aux requêtes imbriquées.

Les commandes suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées (dans l’URL de la requête ou dans `catalog::Modifier` ou `catalog::PostModifier`) :

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Si l’image de résultat des requêtes imbriquées inclut des données de masque (alpha), elle est transmise au calque d’incorporation en tant que masque de calque.

Sont également ignorés `attribute::MaxPix`et `attribute::DefaultPix` le catalogue d’images qui s’applique à la requête imbriquée.

Le résultat de l’image d’une requête IS imbriquée peut être mis en cache, éventuellement, en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Requêtes de rendu d’image incorporées {#section-69c5548db930412b9b90d9b2951a6969}

Lorsque le rendu des images Scene7 est activé sur le serveur, les demandes de rendu peuvent être utilisées comme sources de calque en les spécifiant dans la commande src= (ou mask=). Utilisez la syntaxe suivante :

` …&src=ir( *[!DNL renderRequest]*)&…`

Le `ir` jeton est sensible à la casse.

*[!DNL renderRequest]* est la requête de rendu d’image habituelle, à l’exclusion du chemin racine HTTP ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les caractères de délimiteur de requête imbriqués ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les commandes de rendu d’image suivantes sont ignorées lorsqu’elles sont spécifiées dans des requêtes imbriquées :

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Sont également ignorés `attribute::MaxPix` et le catalogue `attribute::DefaultPix` de matières qui s’applique à la demande de rendu imbriquée.

Le résultat de l’image d’une requête IR imbriquée peut être mis en cache en option en incluant `cache=on`. Par défaut, la mise en cache des données intermédiaires est désactivée. La mise en cache ne doit être activée que lorsque l’image intermédiaire doit être réutilisée dans une autre requête dans un délai raisonnable. La gestion standard du cache côté serveur s’applique. Les données sont mises en cache dans un format sans perte.

## Demandes de rendu FXG incorporées {#section-c817e4b4f7da414ea5a51252ca7e120a}

Lorsque le rendu graphique FXG (alias [!DNL AGMServer]) est installé et activé avec Image Serving, les requêtes FXG peuvent être utilisées comme sources de calques en les spécifiant dans `src=` (ou `mask=`) les commandes. Utilisez la syntaxe suivante :

`…&src=fxg( renderRequest)&…`

Le `fxg` jeton est sensible à la casse.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Le rendu des graphiques FXG n’est disponible que dans les  hébergés  Scene7 et peut nécessiter une licence supplémentaire. Pour plus d’informations, contactez l’assistance technique de Scene7.

*[!DNL renderRequest]* est la requête de rendu FXG habituelle, à l’exclusion du chemin racine HTTP ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
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

Pour spécifier une URL étrangère pour une commande `src=` ou une `mask=` commande, délimitez l’URL ou le fragment d’URL étranger par des parenthèses :

`…&src=( foreignUrl)&…`

Important Les caractères de délimiteur ( `'(',')'`) et les caractères de délimiteur de commande ( `'?'`, `'&'`, `'='`) dans les requêtes imbriquées ne doivent pas être encodés en HTTP. En effet, les requêtes incorporées doivent être codées de la même manière que la requête externe (incorporation).

Les URL absolues complètes (si `attribute::AllowDirectUrls` elles sont définies) et les URL relatives à `attribute::RootUrl` sont autorisées. Une erreur se produit si une URL absolue est incorporée et un attribut : `AllowDirectUrls` est 0 ou si une URL relative est spécifiée et `attribute::RootUrl` est vide.

Bien que les URL étrangères ne puissent pas être spécifiées directement dans le composant de chemin d’accès de l’URL de requête, il est possible de configurer une règle de prétraitement pour permettre la conversion des chemins relatifs en URL absolues (voir l’exemple ci-dessous).

Les images étrangères sont mises en cache par le serveur en fonction des en-têtes de mise en cache inclus dans la réponse HTTP. Si aucun en-tête de réponse HTTP `ETag` ou Last-Modified n’est présent, la réponse n’est pas mise en cache. Cela peut entraîner des performances médiocres pour les accès répétés pour la même image étrangère, car le service d’images doit récupérer et revalider l’image à chaque accès.

Ce mécanisme prend en charge les mêmes formats de fichier image que ceux pris en charge par l’utilitaire de conversion d’image (IC), à l’exception des images source avec 16 bits par composant.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Image Serving exécute automatiquement l’utilitaire de validation lorsqu’une image étrangère est utilisée pour la première fois, afin de s’assurer que l’image est valide et n’a pas été endommagée pendant la transmission. Cela peut entraîner un léger retard lors du premier accès. Pour de meilleures performances, il est recommandé de limiter la taille de ces images et/ou d’utiliser un format de fichier image qui se compresse correctement.

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

La taille de l’image générée par les requêtes imbriquées/incorporées est généralement optimisée automatiquement. Si la mise en cache des images de requête imbriquée est activée, des gains de performances incrémentiels peuvent être réalisés en spécifiant la taille exacte de l’image imbriquée, de sorte qu’aucune mise à l’échelle supplémentaire n’est requise lorsque l’entrée de cache est réutilisée.

Important Image Serving ne prend pas en charge le -codage des requêtes imbriquées ou incorporées. Les requêtes imbriquées et incorporées doivent être codées en HTTP, tout comme les requêtes simples.

## Exemples {#section-d800cfc31abe46d2a964f8e7929231f1}

**Modèle de mise en page avec mise en cache :**

Utilisez l’imbrication pour ajouter la mise en cache à un modèle de calque. Un nombre limité d’images d’arrière-plan sont superposées avec du texte très variable. La chaîne de modèle initiale peut se présenter comme suit :

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Avec de légères modifications, nous pouvons pré-dimensionner l’image du calque 0 et la mettre en cache de manière permanente, réduisant ainsi la charge du serveur :

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Incorporation de requêtes pour le rendu d’image Scene7**

Utilisation d&#39;un modèle stocké dans [!DNL myCatalog/myTemplate]; générez l’image pour layer2 du modèle à l’aide du rendu d’image Scene7 :

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Notez les accolades imbriquées. La demande de rendu d’image incorpore un appel à Image Serving pour récupérer une texture répétable.

## Voir aussi {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference, [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Image Serving Utilities[](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
