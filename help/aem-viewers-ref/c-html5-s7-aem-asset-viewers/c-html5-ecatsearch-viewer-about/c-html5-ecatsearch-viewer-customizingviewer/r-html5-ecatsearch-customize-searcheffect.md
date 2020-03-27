---
description: Le lecteur affiche les régions de résultats de recherche sur le principal pour mettre en surbrillance les mots ou les expressions trouvés dans le catalogue.
seo-description: Le lecteur affiche les régions de résultats de recherche sur le principal pour mettre en surbrillance les mots ou les expressions trouvés dans le catalogue.
seo-title: Effet de recherche
solution: Experience Manager
title: Effet de recherche
topic: Dynamic media
uuid: 3a076ff8-2da5-4020-8a77-8f5a256afefe
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Effet de recherche{#search-effect}

Le lecteur affiche les régions de résultats de recherche sur le principal pour mettre en surbrillance les mots ou les expressions trouvés dans le catalogue.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

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
   <td colname="col1"> <p> <span class="codeph"> arrière-plan </span> </p> </td> 
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

