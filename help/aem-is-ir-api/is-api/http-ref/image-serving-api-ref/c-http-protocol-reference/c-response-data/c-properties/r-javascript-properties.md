---
description: Si javascript est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées en tant que fichier d’inclusion JavaScript.
seo-description: Si javascript est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées en tant que fichier d’inclusion JavaScript.
seo-title: Propriétés JavaScript
solution: Experience Manager
title: Propriétés JavaScript
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Propriétés JavaScript{#javascript-properties}

Si javascript est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées en tant que fichier d’inclusion JavaScript.

Voici la structure générale d’une réponse de propriétés JavaScript type :

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne et avant et après le séparateur =. Toutes les valeurs sont entourées de guillemets simples. Les guillemets simples des chaînes sont placés en séquence d’échappement avec deux guillemets simples consécutifs.

Pour analyser une réponse de propriétés JavaScript, tout objet référencé dans la réponse doit être créé avant le chargement du fichier de propriétés. Voici un exemple d’utilisation de `req=props` pour obtenir la taille de l’image de réponse dans JavaScript :

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

