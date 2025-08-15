---
description: Contrôle du cache. Permet de désactiver sélectivement la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne [!DNL Platform Server] .
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# cache{#cache}

Contrôle du cache. Permet de désactiver sélectivement la mise en cache côté client (navigateur, serveurs proxy, systèmes de mise en cache réseau) et la mise en cache dans le cache interne [!DNL Platform Server] .

`&cache= *`Contrôle du cache`*`

`&cache= *`Contrôle client Contrôle`*, *`du serveur`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Contrôle du cache</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> activé|désactivé</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> contrôle client</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activé|désactivé</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Contrôle serveur</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activé|désactivé</span> </p></td> 
 </tr> 
</table>

Si une *`cacheControl`* seule valeur est spécifiée, elle est appliquée aux caches client et serveur.

Attribut de requête. Ignoré lorsque la demande ne renvoie pas d’image de réponse. *`clientControl`* est ignorée lorsque la mise en cache côté client est désactivée par le catalogue d’images (si `catalog::Expiration` a une valeur négative).

La valeur par défaut est .`cache=on,on`
