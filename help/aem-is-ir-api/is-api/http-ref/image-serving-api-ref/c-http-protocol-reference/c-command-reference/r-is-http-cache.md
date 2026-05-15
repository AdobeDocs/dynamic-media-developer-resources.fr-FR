---
title: cache
description: Contrôle de cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache  [!DNL Platform Server]  interne.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
TQID: 'https://experienceleague.adobe.com/-52nQ085AMsFuqDNv8JdEtXjwYFtIr3aXfHlrERSDoI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 1%

---

# cache{#cache}

Contrôle de cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache [!DNL Platform Server] interne.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activé|désactivé</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activé|désactivé</span> </p></td> 
 </tr> 
</table>

Si une seule valeur `*`cacheControl`*` est spécifiée, elle est appliquée aux caches client et serveur.

Le mot-clé `validate` permet de mettre à jour les entrées du cache après modification des fichiers image, sans avoir à attendre que l’entrée du cache expire automatiquement. La mise en cache du client n’est pas affectée par cette commande.

Le mot-clé `update` peut être utilisé pour forcer la mise à jour des entrées du cache côté serveur. Cela s’avère utile après la modification de ressources qui ne sont pas suivies directement par le mécanisme de validation du cache, par exemple lorsqu’un fichier de police est modifié sans changer son nom de fichier ou l’identifiant de police associé.

Si cela est spécifié dans une requête imbriquée, `cache=on` permet la mise en cache persistante côté serveur de l’image générée par la requête imbriquée. Veillez à activer la mise en cache des requêtes imbriquées uniquement lorsqu’il est prévu d’appeler à plusieurs reprises une même requête imbriquée avec exactement les mêmes paramètres.

## Propriétés {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Attribut de requête. S’applique quel que soit le paramètre de calque actuel. Ignoré lorsque la requête ne renvoie pas d’image de réponse. *`clientControl`* est ignoré lorsque la mise en cache côté client est désactivée par le catalogue d’images (si `catalog::Expiration` a une valeur négative).

Le contrôle du cache côté client ( `on` et `off` uniquement) est également disponible pour les requêtes de contenu statique en [!DNL /is/content/].

## Par défaut {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` pour les requêtes HTTP, `cache=off` pour les requêtes imbriquées/intégrées `cache=on` pour les requêtes de contenu statique.

## Voir aussi {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
