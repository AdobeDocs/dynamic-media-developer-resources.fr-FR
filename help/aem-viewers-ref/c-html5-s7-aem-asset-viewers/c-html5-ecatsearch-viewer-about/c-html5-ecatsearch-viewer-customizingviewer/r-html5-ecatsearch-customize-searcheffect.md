---
description: La visionneuse affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou expressions trouvés dans le catalogue.
solution: Experience Manager
title: Effet de recherche
feature: Dynamic Media Classic,Visionneuses,SDK/API,Recherche catalogue électronique
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# Effet de recherche{#search-effect}

La visionneuse affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou expressions trouvés dans le catalogue.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect des régions de résultats de recherche est contrôlé à l’aide du sélecteur de classe CSS suivant :

`.s7ecatalogsearchviewer .s7searcheffect .s7region`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> propriété CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan de la région des résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple : pour configurer des régions de résultats de recherche avec un remplissage jaune semi-transparent :

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```
