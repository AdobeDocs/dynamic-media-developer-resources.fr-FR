---
description: Paramètre commun à toutes les visionneuses.
solution: Experience Manager
title: initialFrame
feature: Dynamic Media Classic,Visionneuses,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---

# initialFrame{#initialframe}

Paramètre commun à toutes les visionneuses.

>[!NOTE]
>
>Cette commande ne s’applique pas à la visionneuse d’images vidéo.

` initialFrame= *`frameIdx`*[ *`, pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie un index d’image de base zéro que la visionneuse affiche au chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Index de base zéro de la page dans la fenêtre lorsque l’appareil est en orientation portrait. Dans un environnement "de gauche à droite", <span class="codeph"> 0</span> signifie "page de gauche" et <span class="codeph"> 1</span> signifie "page de droite". Dans "de droite à gauche", c'est l'inverse : <span class="codeph"> 0</span> signifie "page de droite" et <span class="codeph"> 1</span> signifie "page de gauche". </p> <p>Si elle n’est pas spécifiée, <span class="codeph"> 0</span> est utilisé par défaut. Ignoré lorsque l’appareil est en orientation paysage. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

Aucune valeur par défaut.

## Exemple {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
