---
description: Zoom sur les données de la cible. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de visionneuse de zoom.
solution: Experience Manager
title: Cibles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---

# Cibles{#targets}

Zoom sur les données de la cible. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de visionneuse de zoom.

Le serveur renvoie le contenu de ce champ en réponse à `req=targets`, après avoir remplacé les jetons de terminaison d’enregistrement &quot; `??`&quot;.

Jusqu’à quatre propriétés peuvent être associées à chaque cible de zoom :

` Target. *`num`*.frame= *`frame`*`

` Target. *`num`*.rect= *`left,top,width,height`*`

` Target. *`num`*.label= *`label`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Nombre cible de zoom (int) ; les cibles de zoom doivent être numérotées de manière séquentielle et consécutive, en commençant par 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> image </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro d’image/de page facultatif pour le ciblage d’une image/page spécifique d’une visionneuse à 360° ou d’une visionneuse de brochures ; la valeur par défaut est 0 si elle n’est pas spécifiée pour la visionneuse à 360° et la visionneuse de brochures ; elle est ignorée par la visionneuse de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> à gauche, haut </span> </span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels du coin supérieur gauche de l’image vers le coin supérieur gauche du rectangle de la cible de zoom (int, int) ; doit être égal ou supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width, height </span> </span> </p> </td> 
  <td class="stentry"> <p>Taille en pixels du rectangle de la cible de zoom (int, int) ; doit être supérieure à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de données texte ; peut être utilisée comme libellé de texte pour un lien de cible de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de données texte ; peut être utilisée pour transmettre des informations spécifiques à la cible au client, telles qu’une valeur de SKU ou une URL de lien dynamique. </p> </td> 
 </tr> 
</table>

Cible. *`num`*.rect est requis pour chaque cible de zoom et doit spécifier un rectangle entièrement dans l’image. Toutes les autres propriétés sont facultatives.

*`label`* et *`userData`* participent à la localisation de la chaîne de texte. Pour plus d’informations, reportez-vous à la section [Localisation de chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans la *référence de protocole HTTP*.

Pour les applications impliquant les clients de visionneuse à 360° et de brochures, les cibles de zoom doivent être définies dans le même enregistrement catalogue qui définit la visionneuse d’images. Toute définition de cible de zoom dans les enregistrements de catalogue des membres de la visionneuse d’images est ignorée par la visionneuse.

Les visionneuses Dynamic Media s’attendent à des cibles de zoom dans les coordonnées de l’image à résolution complète déjà ajustée par les commandes de `catalog::Modifier`.

## Propriétés {#section-b3f8eba4985f4b00bb935d592fe770f9}

Valeur [Property data](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md).

## Par défaut {#section-feab29f6575e482391086a57f547543c}

Aucune

## Voir aussi {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localisation de chaîne de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
