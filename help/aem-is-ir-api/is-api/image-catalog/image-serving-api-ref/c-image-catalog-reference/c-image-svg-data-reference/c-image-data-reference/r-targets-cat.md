---
description: Zoom sur les données de la cible. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de visionneuse de zoom.
solution: Experience Manager
title: Cibles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
TQID: 'https://experienceleague.adobe.com/kP22kltIPZqErqxNKpYp2eNkII-GdYQQeiVH3wEYOvM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 1%

---

# Cibles{#targets}

Zoom sur les données de la cible. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de visionneuse de zoom.

Le serveur renvoie le contenu de ce champ en réponse à `req=targets`, après avoir remplacé les jetons de terminaison d’enregistrement « `??` ».

Vous pouvez associer jusqu’à quatre propriétés à chaque cible de zoom :

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro de la cible du zoom (int) : les cibles du zoom doivent être numérotées de manière séquentielle et consécutive, en commençant par 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cadre </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro d’image/de page facultatif pour le ciblage d’une image/d’une page spécifique d’une visionneuse à 360° ou d’une brochure ; la valeur par défaut est 0 si ce paramètre n’est pas spécifié pour l’utilisation de la visionneuse à 360° ou de brochures ; ignoré par la visionneuse à zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> gauche, haut </span> </span> </p> </td> 
  <td class="stentry"> <p>Décalage en pixels entre le coin supérieur gauche de l’image et le coin supérieur gauche du rectangle cible du zoom (int, int) ; doit être égal ou supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largeur, hauteur </span> </span> </p> </td> 
  <td class="stentry"> <p>Taille en pixels du rectangle cible du zoom (int, int) ; doit être supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de données texte pouvant être utilisée comme libellé de texte pour un lien cible zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de données texte ; peut être utilisée pour transmettre au client des informations spécifiques à la cible, telles qu’une valeur de SKU ou une URL de lien dynamique. </p> </td> 
 </tr> 
</table>

Cible. *`num`*.rect est requis pour chaque cible de zoom et doit spécifier un rectangle dans l’image. Toutes les autres propriétés sont facultatives.

*`label`* et *`userData`* participent à la localisation des chaînes de texte. Pour plus d’informations](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) consultez la section [Localisation de chaîne de texte dans la section *Référence du protocole HTTP*.

Pour les applications impliquant les clients de visionneuse à 360° et de brochure, les cibles de zoom doivent être définies dans le même enregistrement de catalogue qui définit la visionneuse d’images. Toute définition de cible de zoom dans les enregistrements de catalogue des membres de la visionneuse d’images est ignorée par la visionneuse.

Les visionneuses Dynamic Media s’attendent à ce que les cibles de zoom se trouvent dans les coordonnées de l’image en pleine résolution déjà ajustées par les commandes de `catalog::Modifier`.

## Propriétés {#section-b3f8eba4985f4b00bb935d592fe770f9}

Valeur [Property data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md).

## Par défaut {#section-feab29f6575e482391086a57f547543c}

Aucune

## Voir aussi {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
