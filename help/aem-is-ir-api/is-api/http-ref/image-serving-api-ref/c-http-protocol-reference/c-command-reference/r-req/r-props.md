---
description: Propriétés des données de réponse. Évalue la requête en cours comme s’il s’agissait d’une demande d’image (req=img), mais au lieu de renvoyer l’image, le serveur renvoie les propriétés sélectionnées de l’image de réponse.
solution: Experience Manager
title: props
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
TQID: 'https://experienceleague.adobe.com/grTKxMVRKQ8-casDC-aGK6xeQQwqsg2sRLRBGlTrXdc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 5%

---

# props{#props}

Propriétés des données de réponse. Évalue la requête en cours comme s’il s’agissait d’une demande d’image (req=img), mais au lieu de renvoyer l’image, le serveur renvoie les propriétés sélectionnées de l’image de réponse.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p> </td> 
 </tr> 
</table>

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

Voir [Propriétés](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) pour une description de la syntaxe de réponse et du type MIME de réponse. La réponse HTTP peut être mise en cache avec une TTL basée sur `attribute::NonImgExpiration`.

Les propriétés suivantes sont renvoyées pour les requêtes /is/image :

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> la propriété </b> </td> 
   <td> Type de </b> <b></td> 
   <td> <b> Description </b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> hexadécimal </p> </td> 
   <td> <p> Couleur d’arrière-plan (voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Hauteur de l’image de réponse en pixels </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> Cette propriété a la valeur True si le profil ICC est incorporé dans l’image de réponse. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Nom/description du profil associé à l’image de réponse. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Taille de réponse en pixels ne comprenant pas l’en-tête HTTP ; 0 si les données de l’image de réponse n’ont pas été précédemment mises en cache par le serveur. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> énumération </p> </td> 
   <td> <p> 1 si l’image de réponse comprend une couche alpha, 0 dans le cas contraire. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Le type d’image de réponse peut être <span class="codeph"> </span> CMJN, <span class="codeph"> RGB </span> ou <span class="codeph"> BW </span> (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image de réponse contient des chemins, 0 dans le cas contraire. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> Résolution d’impression (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Qualité du JPEG. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Type MIME de l’image de réponse. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Largeur de l’image de réponse en pixels. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image de réponse contient des données xmp, 0 dans le cas contraire. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Identifiant de la version de l’image. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Identifiant de version des métadonnées. (Voir <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

Les propriétés suivantes sont renvoyées pour les requêtes `/is/content` :

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> la propriété </b> </td> 
   <td> Type de </b> <b></td> 
   <td> <b> Description </b> </td> 
  </tr> 
  <tr> 
   <td> <p> </span> du chemin d’accès <span class="codeph"> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p>Chemin du fichier partiellement résolu. (Voir <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> </span> de longueur <span class="codeph"> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Taille du fichier objet en octets </p> </td> 
  </tr> 
  <tr> 
   <td> <p> </span> d’expiration du <span class="codeph"> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> static::Expiration </span> ou la durée de vie par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Date/heure de modification (à partir de <span class="codeph"> </span> static::TimeStamp ou du fichier d’objet) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType </span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> <span class="codeph"> static::UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
