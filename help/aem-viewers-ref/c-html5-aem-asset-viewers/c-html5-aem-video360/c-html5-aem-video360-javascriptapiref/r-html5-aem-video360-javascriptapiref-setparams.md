---
title: setParams
description: JavaScript référence de l’API pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3c228b84-fbad-434f-96b4-d52485711844
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 3%

---

# setParams{#setparams}

JavaScript référence de l’API pour la visionneuse Video360.

` setParams( *`paramètres`*)`

Définit un ou plusieurs paramètres sur une valeur donnée. La syntaxe de l’argument de méthode est identique à une chaîne de requête d’URL. Autrement dit, il représente les paires nom=valeur séparées par `&`. Comme dans une chaîne de requête, les noms et les valeurs sont codés en pourcentage au moyen du codage UTF8. Avant d’appeler `init()`, ce paramètre doit être appelé.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises `config` avec l’objet JSON au constructeur.

Voir aussi [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Paramètre {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"></span> paramètres </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{string}</span> paires de paramètres name=value séparées par <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
