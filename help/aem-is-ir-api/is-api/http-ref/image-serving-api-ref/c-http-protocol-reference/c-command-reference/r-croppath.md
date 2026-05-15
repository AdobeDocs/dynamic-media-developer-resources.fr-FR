---
title: cropsPathE
description: Permet de recadrer dans le cadre de sélection d’un chemin nommé incorporé. Ce recadrage modifie à son tour la taille de l’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78e9f994-d638-49a7-ac42-3146e47210e3
TQID: 'https://experienceleague.adobe.com/zjmnN-7ACO78rMKs7H2S6b989IEHi2I9nPrS5FPaEFA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 1%

---

# cropsPathE{#croppathe}

Permet de recadrer dans le cadre de sélection d’un chemin nommé incorporé. Ce recadrage modifie à son tour la taille de l’image.

`cropPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nom du chemin incorporé dans l’image source du calque (ASCII uniquement). </p> <p> <span class="codeph"><span class="varname"> pathName</span></span> est le nom d’un chemin d’accès incorporé dans l’image source du calque. Le chemin est automatiquement transformé selon les besoins pour maintenir un alignement relatif avec le contenu de l’image. Si plusieurs <span class="codeph"><span class="varname"> pathName</span></span> sont spécifiés, le serveur recadre le cadre de délimitation de chaque chemin, un par un. Tout <span class="codeph"><span class="varname"> pathName</span></span> introuvable dans l’image source est ignoré. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Attribut de calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Ignoré par les calques d’effet.

`cropPathE=` est ignoré si aucun chemin portant le nom spécifié n’est trouvé dans l’image source du calque ou si la source du calque n’est pas une image.

## Par défaut {#section-d1986aa31af14767aeb1b4a57add67f4}

Aucun, pour aucun recadrage supplémentaire du calque.

## Voir aussi {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[recadrage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab), [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
