---
title: Barre de contrôle
description: La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton de lecture/pause et les commandes de volume, et se trouve derrière elles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
TQID: 'https://experienceleague.adobe.com/xWTbcn5GR0BexFz9tX8hy0aElmGPEcAsUhWJ-VSLqI0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 0%

---

# Barre de contrôle{#control-bar}

La barre de contrôle est la zone rectangulaire qui contient toutes les commandes de l’interface utilisateur disponibles pour la visionneuse de vidéos, telles que le bouton de lecture/pause et les commandes de volume, et se trouve derrière elles.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barre de contrôle utilise toujours toute la largeur de visionneuse disponible. Il est possible de modifier sa couleur, sa hauteur et sa position verticale par CSS, par rapport au conteneur de la visionneuse vidéo.

Le sélecteur de classe CSS suivant contrôle l’aspect de la barre de contrôle :

```
.s7video360viewer .s7controlbar
```

## Propriétés CSS de la barre de contrôle {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position à partir de la bordure supérieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> inférieur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Position à partir de la bordure inférieure, y compris la marge intérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de hauteur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Hauteur de la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p>Couleur d’arrière-plan de la barre de contrôle. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple** - Pour configurer une visionneuse de vidéos avec une barre de contrôle grise de 30 pixels de haut située en haut du conteneur de la visionneuse de vidéos.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
