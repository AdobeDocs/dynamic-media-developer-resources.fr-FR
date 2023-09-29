---
title: type
description: Filtre de type contenu statique. Spécifie une chaîne de filtre pour le contenu statique diffusé via /is/content.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9015d5f4-e42c-43e0-af85-fc9c278448e7
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 4%

---

# type{#type}

Filtre de type contenu statique. Spécifie une chaîne de filtre pour le contenu statique diffusé via /is/content.

`type= *`val`*`

<table id="simpletable_B66354A826434A678F3DBC686A0F1436"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Saisissez la chaîne de filtre. </p></td> 
 </tr> 
</table>

Le serveur compare `val` avec la valeur de `catalog::Type` de l’élément de contenu statique demandé. L’élément est renvoyé au client si les valeurs correspondent (sensible à la casse), sinon une erreur est renvoyée.

## Propriétés {#section-529b088434a44a9f86a64ef548d2925b}

Prise en charge uniquement pour les demandes de contenu statique (autres que des images) diffusées via . Ignoré si `catalog::Type` est vide ou non défini.

## Par défaut {#section-e9e8f51d0a01452183ccb510efd87d46}

Aucune correspondance de type n’est appliquée si `type=` n’est pas spécifié ou est vide.

## Voir aussi {#section-da60777a46a74f1bbfa5b2f3b240eb0f}

[Diffusion de contenu statique (hors image)](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-serving-static-non-image-content.md#reference-cbe50e697fdf4c7bbb0084f98b7739da), [catalog::UserType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-usertype-cat.md)
