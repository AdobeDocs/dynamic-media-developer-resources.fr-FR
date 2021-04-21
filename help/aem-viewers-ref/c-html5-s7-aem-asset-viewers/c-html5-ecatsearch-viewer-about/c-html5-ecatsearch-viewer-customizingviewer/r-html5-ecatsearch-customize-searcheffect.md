---
description: Le lecteur affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou les expressions figurant dans le catalogue.
solution: Experience Manager
title: Effet de recherche
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 1%

---


# Effet de recherche {#search-effect}

Le lecteur affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou les expressions figurant dans le catalogue.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visualisation principale**

L’aspect des régions de résultats de recherche est contrôlé par le sélecteur de classe CSS suivant :

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
   <td colname="col1"> <p> <span class="codeph"> arrière  </span> </p> </td> 
   <td colname="col2"> <p>Arrière-plan de la région des résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemple - pour configurer des régions de résultats de recherche avec un remplissage jaune semi-transparent :

```
.s7ecatalogsearchviewer .s7searcheffect .s7region { 
 background: rgba(255,255,0, 0.5); 
}
```

