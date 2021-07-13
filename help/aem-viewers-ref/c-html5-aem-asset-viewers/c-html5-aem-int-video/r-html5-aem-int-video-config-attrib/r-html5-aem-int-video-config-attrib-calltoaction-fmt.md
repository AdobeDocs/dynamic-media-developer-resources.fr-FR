---
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 5%

---

# CallToAction.fmt{#calltoaction-fmt}

Attribut de configuration de la visionneuse de vidéos interactives.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Indique le format d’image que le composant utilise pour charger les images à partir du serveur d’images. </p> <p>Si le format spécifié se termine par "<span class="codeph"> -alpha</span>", le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```
