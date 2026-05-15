---
title: Infobulles
description: Sur les ordinateurs de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des info-bulles qui s’affichent lorsque vous pointez dessus.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 6367245a-be55-4b7e-bf9e-da4a0ecb556b
TQID: 'https://experienceleague.adobe.com/-0X46-2wUL9anT3IP3k8IueGloXk8EdsnHhopc7gzrw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# Infobulles{#tooltips}

Sur les ordinateurs de bureau, certains éléments de l’interface utilisateur tels que les boutons comportent des info-bulles qui s’affichent lorsque vous pointez dessus.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Propriétés CSS de la zone de visionneuse principale**

L’aspect des infobulles est contrôlé avec le sélecteur de classe CSS suivant :

```
.s7tooltip
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
   <td colname="col1"> <p> </span> de rayon de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Rayon de la bordure d'arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur de bordure <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Couleur de la bordure d’arrière-plan. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> des </span> de couleur d’arrière-plan </p> </td> 
   <td colname="col2"> <p> Couleur de fond. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de couleur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Couleur du texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> famille de polices </p> </td> 
   <td colname="col2"> <p>Nom de la police de texte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> de taille de police <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Taille de police du texte. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Si les styles d’info-bulle sont personnalisés à partir de la page web d’incorporation, toutes les propriétés doivent contenir `!IMPORTANT` règle. Cette règle n’est pas nécessaire si les infobulles sont personnalisées dans le fichier CSS de la visionneuse.

Exemple - pour configurer des info-bulles dont la bordure grise présente un rayon de trois pixels, un arrière-plan noir et un texte blanc écrit en Arial®, taille de 11 pixels :

```
.s7tooltip { 
 border-radius: 3px 3px 3px 3px; 
 border-color: #999999; 
 background-color: #000000; 
 color: #FFFFFF; 
 font-family: Arial, Helvetica, sans-serif; 
 font-size: 11px; 
}
```
