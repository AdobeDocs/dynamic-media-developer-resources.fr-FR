---
description: Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.
seo-description: Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.
seo-title: cache
solution: Experience Manager
title: cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on| désactivé| validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on| désactivé </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on| désactivé </p></td> 
 </tr> 
</table>

Si une seule *`cacheControl`* valeur est spécifiée, elle est appliquée aux caches client et serveur.

Le mot-clé &quot; `validate`&quot; permet de mettre à jour les entrées de cache du serveur après modification des fichiers de texture ou de vignette, sans avoir à attendre que l&#39;entrée de cache expire automatiquement. La mise en cache du client n’est pas affectée par cette commande.

S’il est spécifié dans une requête imbriquée, `cache=on` active la mise en cache persistante côté serveur de l’image générée par la requête imbriquée. Veillez à activer la mise en cache pour les requêtes imbriquées uniquement lorsque la même requête imbriquée doit être appelée à plusieurs reprises avec exactement les mêmes paramètres.

## Propriétés {#section-0dcbd62e1122400e8c347f408f2d937e}

Peut se produire n’importe où dans la requête. Ignoré lorsque la requête ne renvoie pas d’image de réponse. *`clientControl`* est ignorée lorsque la mise en cache côté client est désactivée par le catalogue de matières (si `attribute::Expiration` la valeur est négative). *`serverControl`* est ignorée si la mise en cache du serveur est désactivée ( `PlatformServer::cache.enable`).

## Par défaut {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` pour les requêtes HTTP, `cache=off` pour les requêtes imbriquées/incorporées.

## Voir aussi {#section-2f5853751dab49579e97418fa766bdf9}

[catalogue ::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
