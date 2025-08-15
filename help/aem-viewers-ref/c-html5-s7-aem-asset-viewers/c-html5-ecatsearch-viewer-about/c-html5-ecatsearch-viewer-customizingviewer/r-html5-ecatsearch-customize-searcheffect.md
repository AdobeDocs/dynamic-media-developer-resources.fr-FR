---
title: Effet de recherche
description: La visionneuse affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou expressions trouvés dans le catalogue.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---

# Effet de recherche{#search-effect}

La visionneuse affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou expressions trouvés dans le catalogue.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect des régions de résultats de recherche est contrôlé avec le sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> d’arrière-plan </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan de la région des résultats de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer des zones de résultats de recherche avec un remplissage jaune semi-transparent :

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
