---
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-description: Référence de l’API JavaScript pour la visionneuse de vidéos.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic media
uuid: 0497ae9c-e94a-458d-a4c7-5915add17f60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParams{#setparams}

Référence de l’API JavaScript pour la visionneuse de vidéos.

` setParams( *`params`*)`

Définit un ou plusieurs paramètres sur une valeur donnée. La syntaxe de l’argument de méthode est identique à une chaîne de d’URL. Autrement dit, il représente les paires nom=valeur séparées par `&`. Comme dans une chaîne de , les noms et les valeurs sont codés en pourcentage à l’aide de UTF8. Avant d’appeler `init()`, ce paramètre doit être appelé.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet `config` JSON au constructeur.

Voir aussi [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=value, paires de paramètres séparées par <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```

