---
description: Le lecteur affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou les expressions figurant dans le catalogue.
seo-description: Le lecteur affiche les régions de résultats de recherche sur la vue principale pour mettre en surbrillance les mots ou les expressions figurant dans le catalogue.
seo-title: Effet de recherche
solution: Experience Manager
title: Effet de recherche
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
feature: Dynamic Media Classic, Visionneuses, SDK/API, Recherche de catalogue électronique
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

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

