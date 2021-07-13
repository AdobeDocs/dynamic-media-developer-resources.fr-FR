---
description: Si JavaScript™ est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées sous la forme d’un fichier d’inclusion JavaScript™.
solution: Experience Manager
title: Propriétés JavaScript™
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# Propriétés JavaScript™{#javascript-properties}

Si JavaScript™ est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées sous la forme d’un fichier d’inclusion JavaScript™.

Une réponse de propriétés JavaScript™ standard présente la structure générale suivante :

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne, avant et après le séparateur = . Toutes les valeurs sont entourées de guillemets simples. Les guillemets simples des chaînes sont précédés de deux guillemets simples consécutifs.

Pour analyser une réponse de propriétés JavaScript™, tout objet ou objet référencé dans la réponse doit être créé avant le chargement du fichier de propriétés. Voici un exemple d’utilisation de `req=props` pour obtenir la taille de l’image de réponse dans JavaScript™ :

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
