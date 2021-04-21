---
description: Données de cible de zoom. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de la visionneuse de zoom.
solution: Experience Manager
title: Cibles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 2%

---


# Cibles{#targets}

Données de cible de zoom. Aucune ou plusieurs propriétés de cible de zoom, qui peuvent être utilisées conjointement avec le client de la visionneuse de zoom.

Le serveur renvoie le contenu de ce champ en réponse à `req=targets`, après avoir remplacé les jetons de terminaison d&#39;enregistrement &quot; `??`&quot;.

Jusqu’à quatre propriétés peuvent être associées à chaque cible de zoom :

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro de la cible de zoom (int); les cibles de zoom doivent être numérotées de manière séquentielle et consécutive, en commençant par 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro de cadre/de page facultatif pour le ciblage d’un cadre/d’une page spécifique d’une visionneuse à 360° ou d’une visionneuse de brochures ; la valeur par défaut est 0 si elle n’est pas spécifiée pour l’utilisation de la visionneuse à 360° et de la visionneuse de brochures ; ignorée par la visionneuse de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> gauche, haut  </span> </span> </p> </td> 
  <td class="stentry"> <p>Décalage en pixels du coin supérieur gauche de l’image vers le coin supérieur gauche du rectangle de la cible de zoom (int, int); doit être égal ou supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> largeur, hauteur  </span> </span> </p> </td> 
  <td class="stentry"> <p>Taille en pixels du rectangle de la cible de zoom (int, int); doit être supérieur à 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur des données textuelles ; peut être utilisé comme libellé de texte pour un lien de cible de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur des données textuelles ; peut être utilisé pour transmettre des informations spécifiques à une cible au client, telles qu’une valeur SKU ou une URL de lien à chaud. </p> </td> 
 </tr> 
</table>

Cible. *`num`*.rect est requis pour chaque cible de zoom et doit spécifier un rectangle entièrement dans l’image. Toutes les autres propriétés sont facultatives.

*`label`* et  *`userData`* participer à la localisation de chaînes de texte. Pour plus d&#39;informations, consultez la [Localisation de chaînes de texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) dans le *Guide de référence du protocole HTTP*.

Pour les applications impliquant les clients des visionneuses à 360° et des lecteurs de brochures, les cibles de zoom doivent être définies dans le même enregistrement de catalogue qui définit la visionneuse d’images. Toute définition de cible de zoom figurant dans les enregistrements de catalogue des membres de la visionneuse d’images est ignorée par la visionneuse.

Les visionneuses Dynamic Media s’attendent à ce que les cibles de zoom correspondent aux coordonnées de l’image à résolution complète déjà ajustées par les commandes de `catalog::Modifier`.

## Propriétés {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valeur de ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) données de propriété.

## Par défaut {#section-feab29f6575e482391086a57f547543c}

Aucune

## Voir aussi {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalogue ::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catalogue::Modificateur](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localisation de chaîne de  [texte](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
