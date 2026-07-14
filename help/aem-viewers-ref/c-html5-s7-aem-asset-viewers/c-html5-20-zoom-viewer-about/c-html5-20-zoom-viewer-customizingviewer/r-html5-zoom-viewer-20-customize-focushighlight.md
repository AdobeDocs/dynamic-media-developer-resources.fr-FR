---
title: Mettre en surbrillance
description: La mise en surbrillance de la sélection d’entrée affichée autour de l’élément d’IU de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 31fd8022-0072-4a4c-8947-57858a094f3c
TQID: 'https://experienceleague.adobe.com/PscuE1Tv5gYcWvC3Ra7wHjBP1fqqbChpcZhopd3S5EI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 1%

---

# Mettre en surbrillance{#focus-highlight}

La mise en surbrillance de la sélection d’entrée affichée autour de l’élément d’IU de la visionneuse ciblée est contrôlée avec le sélecteur de classe CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS**

L’aspect est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7zoomviewer *:focus
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de plan <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Style de surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - Pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7zoomviewer *:focus { 
 outline: none; 
}
```

