---
description: Informations sur la visionneuse de médias.
solution: Experience Manager
title: définir
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# définir{#set}

Informations sur la visionneuse de médias.

req=set[,xml[, *`encoding`*]|{ json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codage</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | Norme ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identifiant de demande unique </p></td> 
 </tr> 
</table>

Renvoie des informations sur les images, les vidéos, les échantillons et les diverses métadonnées associées à catalog ::ImageSet pour l’entrée de catalogue d’images spécifiée dans le chemin d’URL. Cette réponse est une structure hiérarchique déterminée par le type d’ensemble fourni. Une mise en forme appropriée est appliquée lorsque le format &#39;xml&#39; ou &#39;json&#39; est demandé.

La réponse HTTP peut être mise en cache avec la durée de vie basée sur la base de `catalog::NonImgExpiration`.

>[!NOTE]
>
>Le caractère deux-points n’est pas autorisé dans les requêtes req=set.

Les demandes qui prennent en charge le format de réponse JSON vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.
