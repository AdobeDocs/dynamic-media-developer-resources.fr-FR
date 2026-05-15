---
title: type
description: Filtre de type de contenu statique. Indique une chaîne de filtre pour le contenu statique diffusé au moyen de /is/content.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
TQID: 'https://experienceleague.adobe.com/YudohKBdOo08A1MLfQuILLVhe9mXTAcuzWs5z6zrh-g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 4%

---

# type{#type}

Filtre de type de contenu statique. Indique une chaîne de filtre pour le contenu statique diffusé au moyen de /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Saisissez la chaîne de filtre. </p></td> 
 </tr> 
</table>

Le serveur compare `val` avec la valeur de `catalog::Type` de l’élément de contenu statique demandé. L’élément est renvoyé au client si les valeurs correspondent (sensibles à la casse), sinon une erreur est renvoyée.

## Propriétés {#section-529b088434a44a9f86a64ef548d2925b}

Pris en charge uniquement pour les requêtes de contenu statique (autres que les requêtes d’image) diffusées par le biais de . Ignoré si `catalog::Type` est vide ou non défini.

## Par défaut {#section-e9e8f51d0a01452183ccb510efd87d46}

Aucune correspondance de type n’est appliquée si `type=` n’est pas spécifié ou est vide.

## Voir aussi {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Diffusion de contenu statique (hors images)](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catalog:::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
