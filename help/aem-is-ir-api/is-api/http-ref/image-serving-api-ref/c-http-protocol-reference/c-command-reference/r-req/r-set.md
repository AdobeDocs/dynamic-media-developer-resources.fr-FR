---
description: Informations sur la visionneuse de supports.
seo-description: Informations sur la visionneuse de supports.
seo-title: définir
solution: Experience Manager
title: définir
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# définir{#set}

Informations sur la visionneuse de supports.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encodage</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique </p></td> 
 </tr> 
</table>

Renvoie des informations sur les images, les vidéos, les échantillons et les diverses métadonnées associées à catalog::ImageSet pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès de l’URL. Cette réponse est une structure hiérarchique déterminée par le type d’ensemble fourni. Une mise en forme appropriée est appliquée lorsque le format &quot;xml&quot; ou &quot;json&quot; est demandé.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::NonImgExpiration`.

>[!NOTE]
>
>Le caractère deux-points n’est pas autorisé dans les requêtes req=set.

Les requêtes qui prennent en charge le format de réponse JSON vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Default is `s7jsonResponse`.
