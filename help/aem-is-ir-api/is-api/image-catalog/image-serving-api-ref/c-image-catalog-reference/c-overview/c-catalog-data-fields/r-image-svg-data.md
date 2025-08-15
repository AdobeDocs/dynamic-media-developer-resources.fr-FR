---
description: Les champs suivants sont reconnus dans les fichiers de données image et SVG.
solution: Experience Manager
title: Image_SVG données
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5392e08f-3614-4588-8846-4262d32f3ce1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Image_SVG données{#image-svg-data}

Les champs suivants sont reconnus dans les fichiers de données image et SVG.

## Gestion des catalogues {#section-1056bcc3b6d04166b3aa6ec48913b6b2}

<table id="table_823F89CAD494441690D28F18005F774C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md" type="reference" format="dita" scope="local"> Id</a></span> </p> </td> 
   <td colname="col2"> <p>Identifiant de l’enregistrement du catalogue (clé d’index). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Attributs de requête {#section-cfe69bcdcd4b4d129e99d11b9078ae4a}

<table id="table_C070C676835F49918E1B3BBF81471B09"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba" type="reference" format="dita" scope="local"> DigimarcInfo</a></span> </p> </td> 
   <td colname="col2"> <p>Informations spécifiques à l’image pour l’incorporation Digimarc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a" type="reference" format="dita" scope="local"> Expiration</a></span> </p> </td> 
   <td colname="col2"> <p>Expiration du cache (durée d’activation) pour les images de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md" type="reference" format="dita" scope="local"> Modificateur</a> </span> </p> </td> 
   <td colname="col2"> <p>Modificateurs de demande de préfixe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md" type="reference" format="dita" scope="local"> PostModifier</a> </span> </p> </td> 
   <td colname="col2"> <p>Modificateurs de requête de postfixe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded" type="reference" format="dita" scope="local"> Horodatage</a></span> </p> </td> 
   <td colname="col2"> <p>Horodatage de modification du fichier. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Attributs d’image {#section-74c4d124255d4218ade87d7d1677c76d}

<table id="table_F2A33C2EB17A4EACB00DDEF7FB1BB0D4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md" type="reference" format="dita" scope="local"> Ancre</a></span> </p> </td> 
   <td colname="col2"> <p>Point d’ancrage de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md" type="reference" format="dita" scope="local"> Chemin de masque</a></span> </p> </td> 
   <td colname="col2"> <p>Chemin du fichier de masque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md" type="reference" format="dita" scope="local"> Chemin</a></span> </p> </td> 
   <td colname="col2"> <p>Chemin d’accès au fichier image/SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5" type="reference" format="dita" scope="local"> Imprimer la résolution</a></span> </p> </td> 
   <td colname="col2"> <p>Résolution d’impression. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1" type="reference" format="dita" scope="local"> Résolution</a></span> </p> </td> 
   <td colname="col2"> <p>Résolution d’objet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-size-cat.md" type="reference" format="dita" scope="local"> Taille</a></span> </p> </td> 
   <td colname="col2"> <p>Taille de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Attributs de miniature {#section-c5ac27bcd4224a80b7f42ead249027b1}

<table id="table_E07909B6C16F4D9686ADA381A4178E25"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69" type="reference" format="dita" scope="local"> Pouces</a></span> </p> </td> 
   <td colname="col2"> <p>Résolution des miniatures. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03" type="reference" format="dita" scope="local"> Type de miniature</a></span> </p> </td> 
   <td colname="col2"> <p>Type de miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Données auxiliaires {#section-bff4e1f9af9d45f1872abac3b414a629}

<table id="table_B6A9A702F533494E85CEC1AD42EC728A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-assettype-cat.md" type="reference" format="dita" scope="local"> Type de ressource</a></span> </p> </td> 
   <td colname="col2"> <p>Type de ressource. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md" type="reference" format="dita" scope="local"> Visionneuse d’images</a></span> </p> </td> 
   <td colname="col2"> <p>Données de la visionneuse d’images. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md" type="reference" format="dita" scope="local"> Carte</a></span> </p> </td> 
   <td colname="col2"> <p>Données de zone cliquable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md" type="reference" format="dita" scope="local"> Cibles</a></span> </p> </td> 
   <td colname="col2"> <p>Données de cible de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><a href="/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md" type="reference" format="dita" scope="local"> Données utilisateur</a></span> </p> </td> 
   <td colname="col2"> <p>Données définies par l’utilisateur. </p> </td> 
  </tr> 
 </tbody> 
</table>
