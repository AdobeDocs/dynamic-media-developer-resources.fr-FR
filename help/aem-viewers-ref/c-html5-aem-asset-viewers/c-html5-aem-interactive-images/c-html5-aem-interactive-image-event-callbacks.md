---
title: Rappels d’événement
description: Rappels d’événement
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 59b8a88e-0139-4981-bfb9-f2dc1ac2337d
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# Rappels d’événement{#event-callbacks}

La visionneuse prend en charge les rappels d’événement JavaScript que la page web utilise pour effectuer le suivi du processus d’initialisation de la visionneuse ou du comportement d’exécution.

Les gestionnaires de rappel sont attribués en transmettant les noms d’événement et les fonctions de gestionnaire correspondantes avec la propriété `handlers` à `config`’objet JSON dans le constructeur de la visionneuse. Il est également possible d’utiliser `setHandlers()` méthode API.

Les événements de visionneuse pris en charge sont les suivants :

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evénement de visionneuse </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete </span> </p> </td> 
   <td colname="col2"> <p>Se déclenche lorsque l’initialisation de la visionneuse est terminée et que tous les composants internes sont créés, de sorte qu’il soit possible d’utiliser <span class="codeph">’API getComponent() </span>. Le gestionnaire de rappel ne prend aucun argument. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Se déclenche à chaque fois qu’un événement se produit dans la visionneuse et peut être géré par un système de suivi d’événement, tel qu’Adobe Analytics. Le gestionnaire de rappel accepte les arguments suivants : </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} </span> - non utilisé actuellement. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span> - actuellement non utilisé. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span> - nom d’instance du composant SDK de la visionneuse qui a déclenché l’événement. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number} </span> - horodatage de l'événement. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span> - payload d’événement. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate </span> </p> </td> 
   <td colname="col2"> <p> Se déclenche lorsque l’utilisateur active une zone réactive avec les données d’aperçu rapide qui y sont associées. Le gestionnaire de rappel utilise l’argument suivant : </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object} </span> : objet JSON contenant des données issues de la définition de la zone réactive. Le champ <span class="codeph"> la </span> de sku est obligatoire, tandis que les autres champs sont facultatifs et dépendent de la définition de la zone réactive source. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [InteractiveImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd) et [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
