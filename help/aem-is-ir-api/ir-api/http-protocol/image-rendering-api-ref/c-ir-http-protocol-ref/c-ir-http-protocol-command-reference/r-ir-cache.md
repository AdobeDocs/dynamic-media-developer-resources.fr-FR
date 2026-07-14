---
title: cache
description: Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache  [!DNL Platform Server]  interne.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
TQID: 'https://experienceleague.adobe.com/xq-8hE9RB7I-CMb-yguhBcEttxTv6IRRHWzh0lDvn6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 1%

---

# cache {#cache}

Contrôle du cache. Vous permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache de [!DNL Platform Server] interne.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>activé | désactivé | valider </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>activé | désactivé </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>activé | désactivé </p></td> 
 </tr> 
</table>

Si une seule valeur *`cacheControl`* est spécifiée, elle est appliquée aux caches client et serveur.

Le mot-clé « `validate` » permet de mettre à jour les entrées du cache du serveur une fois que les fichiers de texture ou de vignette ont changé, sans avoir à attendre que l&#39;entrée du cache expire automatiquement. La mise en cache du client n’est pas affectée par cette commande.

Si cela est spécifié dans une requête imbriquée, `cache=on` permet la mise en cache persistante côté serveur de l’image générée par la requête imbriquée. Veillez à activer la mise en cache pour les requêtes imbriquées uniquement lorsque la même requête imbriquée est appelée à plusieurs reprises avec les mêmes paramètres.

## Propriétés {#section-0dcbd62e1122400e8c347f408f2d937e}

Peut se produire n’importe où dans la requête. Ignoré lorsque la requête ne renvoie pas d’image de réponse. La propriété *`clientControl`* est ignorée lorsque la mise en cache côté client est désactivée par le catalogue de matières (si `attribute::Expiration` a une valeur négative). La propriété *`serverControl`* est ignorée si la mise en cache du serveur est désactivée ( `PlatformServer::cache.enable`).

## Par défaut {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Pour les requêtes HTTP, `cache=off` pour les requêtes imbriquées/intégrées.

## Voir aussi {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

