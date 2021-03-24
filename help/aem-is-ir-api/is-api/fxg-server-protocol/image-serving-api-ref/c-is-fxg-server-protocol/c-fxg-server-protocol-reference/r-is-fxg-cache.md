---
description: Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 1%

---


# cache{#cache}

Contrôle du cache. Permet de désactiver de manière sélective la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne du serveur de plateformes.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlServerControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
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

Si une seule valeur *`cacheControl`* est spécifiée, elle est appliquée aux caches client et serveur.

Attribut de requête. Ignoré lorsque la requête ne renvoie pas d’image de réponse. *`clientControl`* est ignorée lorsque la mise en cache côté client est désactivée par le catalogue d’images (si  `catalog::Expiration` la valeur est négative).

Defaults to `cache=on,on`.
