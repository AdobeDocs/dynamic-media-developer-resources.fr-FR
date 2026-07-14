---
title: Effet de recherche
description: La visionneuse affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou expressions trouvés dans le catalogue.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 3591edb0-4b0a-4761-af87-c372132c5138
TQID: 'https://experienceleague.adobe.com/h30DfEeB69i1gbnfOvnKphglRkXgcvOTG8L-eTZv2GU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 85
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
   <td colname="col1"> <p> </span> d’arrière-plan <span class="codeph"> </p> </td> 
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
