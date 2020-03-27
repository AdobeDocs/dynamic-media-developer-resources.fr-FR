---
description: Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.
seo-description: Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.
seo-title: cache
solution: Experience Manager
title: cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Si une seule valeur ` *`cacheControl`*` est spécifiée, elle est appliquée aux caches client et serveur.

Le `validate` mot-clé permet de mettre à jour les entrées du cache après modification des fichiers image, sans avoir à attendre que l’entrée du cache expire automatiquement. La mise en cache du client n’est pas affectée par cette commande.

Le `update` mot-clé peut être utilisé pour forcer la mise à jour des entrées du cache côté serveur. Cela s’avère utile après la modification des ressources qui ne sont pas directement suivies par le mécanisme de validation du cache, par exemple lorsqu’un fichier de police est modifié sans modifier son nom ou l’ID de police associé.

S’il est spécifié dans une requête imbriquée, `cache=on` active la mise en cache persistante côté serveur de l’image générée par la requête imbriquée. Veillez à activer la mise en cache pour les requêtes imbriquées uniquement lorsque la même requête imbriquée doit être appelée à plusieurs reprises avec exactement les mêmes paramètres.

## Propriétés {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Attribut de requête. S’applique indépendamment du paramètre de calque actif. Ignoré lorsque la requête ne renvoie pas d’image de réponse. *`clientControl`*est ignoré lorsque la mise en cache côté client est désactivée par le catalogue d’images (si `catalog::Expiration` la valeur est négative).

Le contrôle du cache côté client ( `on` et `off` uniquement) est également disponible pour les requêtes de contenu statique à [!DNL /is/content/]l’emplacement.

## Par défaut {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` pour les requêtes HTTP, `cache=off` pour les requêtes imbriquées/incorporées `cache=on` pour les requêtes de contenu statique.

## Voir aussi {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogue ::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
