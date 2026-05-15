---
description: Données utilisateur du catalogue d’images. Renvoie les données utilisateur pour l’entrée du catalogue d’images spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
TQID: 'https://experienceleague.adobe.com/cLVsaN--jydZTkV6GA92jN1PO8VOFAEZxhSg7F2S9dk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

---

# userdata{#userdata}

Données utilisateur du catalogue d’images. Renvoie les données utilisateur pour l’entrée du catalogue d’images spécifiée dans le chemin d’accès à l’URL.

`req=userdata[,text|{xml[, *`encodage`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Encodage de </span> <span class="varname"></p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Le contenu de `catalog::UserData` est renvoyé. Lorsque le format &#39;text&#39; est spécifié, toutes les instances de `??` dans `catalog::UserData`sont remplacées par des terminaisons de ligne, et une terminaison d&#39;une seule ligne (CR/LF) est ajoutée à la fin. Si le chemin d’URL ne correspond pas à une entrée de catalogue valide, la réponse se compose uniquement d’une terminaison d’une seule ligne. Une mise en forme appropriée est appliquée lorsque le format « xml » ou « json » est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être mise en cache avec la TTL basée sur `catalog::Expiration`.

>[!NOTE]
>
>Le caractère deux-points n’est pas autorisé dans les noms de clé de propriété des données utilisateur.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
