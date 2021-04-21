---
description: Permet de recadrer le cadre de sélection d’un chemin nommé incorporé. Ce recadrage, à son tour, modifie la taille de l’image.
solution: Experience Manager
title: culturePathE
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# culturePathE{#croppathe}

Permet de recadrer le cadre de sélection d’un chemin nommé incorporé. Ce recadrage, à son tour, modifie la taille de l’image.

`cropPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nom du chemin d’accès incorporé à l’image source du calque (ASCII uniquement). </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName est le nom d’un chemin incorporé à l’image source du calque. Le chemin est automatiquement transformé, si nécessaire, pour conserver un alignement relatif avec le contenu de l’image. Si plusieurs <span class="codeph"><span class="varname"> pathName</span></span> sont spécifiés, le serveur rogne le cadre de sélection de chaque chemin, un par un. Tout <span class="codeph"><span class="varname"> cheminName</span></span> introuvable dans l'image source est ignoré. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attribut de couche. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

`cropPathE=` est ignoré si aucun chemin d’accès portant le nom spécifié n’est trouvé dans l’image source du calque ou si la source du calque n’est pas une image.

## Par défaut {#section-d1986aa31af14767aeb1b4a57add67f4}

Aucun, pour aucun recadrage supplémentaire du calque.

## Voir aussi {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[recadrage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
