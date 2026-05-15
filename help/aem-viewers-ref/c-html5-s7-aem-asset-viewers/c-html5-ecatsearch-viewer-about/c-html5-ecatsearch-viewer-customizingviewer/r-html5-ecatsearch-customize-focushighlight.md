---
title: Mettre en surbrillance
description: Mise en surbrillance de la sélection des entrées affichée autour de l’élément d’interface utilisateur de la visionneuse ciblé.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 949b8a8b-5f59-415e-acc1-bf8cea77cbd9
TQID: 'https://experienceleague.adobe.com/E7n09sJ0qY9Aivp5OUFr5Jc6bwS5Ah3N-HdS9-H2Pgw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 0%

---

# Mettre en surbrillance{#focus-highlight}

Mise en surbrillance de la sélection des entrées affichée autour de l’élément d’interface utilisateur de la visionneuse ciblé.

<!--<a id="section_E8B3D0BF9FF548F188F717D6EA65EC32"></a>-->

L’aspect de la mise en surbrillance est contrôlé par le sélecteur de classe CSS suivant :

```
.s7ecatalogviewer *:focus
```

**Propriétés CSS de la mise en surbrillance du focus**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de plan <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Style de surbrillance du focus. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour désactiver la mise en surbrillance par défaut du navigateur pour tous les éléments de l’interface utilisateur de la visionneuse, ajoutez le sélecteur CSS suivant à la feuille de style de la visionneuse :

```
.s7ecatalogviewer *:focus { 
 outline: none; 
}
```
