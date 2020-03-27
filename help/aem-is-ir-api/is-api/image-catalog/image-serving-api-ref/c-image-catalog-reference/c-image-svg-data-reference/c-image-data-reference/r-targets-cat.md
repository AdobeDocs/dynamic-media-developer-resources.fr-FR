---
description: Zoom  données. Aucune ou plusieurs propriétés de  de zoom, qui peuvent être utilisées conjointement avec le client de la visionneuse de zoom.
seo-description: Zoom  données. Aucune ou plusieurs propriétés de  de zoom, qui peuvent être utilisées conjointement avec le client de la visionneuse de zoom.
seo-title: Cibles
solution: Experience Manager
title: Cibles
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Cibles{#targets}

Zoom  données. Aucune ou plusieurs propriétés de  de zoom, qui peuvent être utilisées conjointement avec le client de la visionneuse de zoom.

Le serveur renvoie le contenu de ce champ en réponse `req=targets`, après avoir remplacé les jetons de terminateur d’enregistrement &#39; `??`&#39;.

Jusqu’à quatre propriétés peuvent être associées à chaque  de zoom :

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span></span> </p> </td> 
  <td class="stentry"> <p>Zoom  nombre (int); les  de zoom doivent être numérotées de manière séquentielle et consécutive, en commençant par 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cadre </span></span> </p> </td> 
  <td class="stentry"> <p>Numéro de cadre/de page facultatif pour le ciblage d’un cadre/d’une page spécifique d’une visionneuse à 360° ou d’une visionneuse de brochures ; la valeur par défaut est 0 si elle n’est pas spécifiée pour l’utilisation de la visionneuse à 360° et de la visionneuse de brochures ; ignorée par la visionneuse de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> gauche, haut </span></span> </p> </td> 
  <td class="stentry"> <p>Décalage des pixels du coin supérieur gauche de l’image vers le coin supérieur gauche du rectangle du de zoom (int, int) ; doit être supérieur ou égal à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largeur, hauteur </span></span> </p> </td> 
  <td class="stentry"> <p>Taille en pixels du rectangle  du de zoom (int, int); doit être supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> libellé </span></span> </p> </td> 
  <td class="stentry"> <p>Valeur des données textuelles; peut être utilisé comme libellé de texte pour un lien de de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span></span> </p> </td> 
  <td class="stentry"> <p>Valeur des données textuelles; peut être utilisée pour transmettre des informations spécifiques à un  au client, telles qu’une valeur SKU ou une URL de lien dynamique. </p> </td> 
 </tr> 
</table>

Cible. *`num`*.rect est requis pour chaque  de zoom et doit spécifier un rectangle entièrement dans l’image. Toutes les autres propriétés sont facultatives.

*`label`* et *`userData`* participez à des  de chaînes de texte. Pour plus d’informations, reportez-vous à la [Chaîne de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texte *dans le Guide de référence* du protocoleHTTP.

Pour les applications impliquant les clients des visionneuses à 360° et à 360°, le de zoom doit être défini dans le même enregistrement de catalogue qui définit la visionneuse d’images. Toute définition de de zoom figurant dans les enregistrements de catalogue des membres de la visionneuse d’images est ignorée par le lecteur.

Les visionneuses Scene7 s’attendent à ce que le de zoom soit  dans les coordonnées de l’image en pleine résolution déjà ajustées par les commandes de `catalog::Modifier`Scene7.

## Propriétés {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valeur des données](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) de propriété.

## Par défaut {#section-feab29f6575e482391086a57f547543c}

Aucune

## Voir aussi {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalogue::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalogue::Modificateur](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), de chaînes de [texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
