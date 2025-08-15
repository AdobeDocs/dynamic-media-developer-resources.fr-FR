---
title: Propriétés de JavaScript
description: Si JavaScript est spécifié comme format de réponse, les données de réponse sont formatées de sorte qu’elles soient analysées en tant que fichier JavaScript&trade; include.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Propriétés de JavaScript{#javascript-properties}

Si JavaScript est spécifié comme format de réponse, les données de réponse sont formatées afin d’être analysées en tant que fichier d’inclusion JavaScript.

Une réponse de propriétés JavaScript standard possède la structure générale suivante :

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

Le *`propertyValue`* peut être vide. L&#39;espace est facultatif au début et à la fin de chaque ligne et avant et après le séparateur =. Toutes les valeurs sont entourées de guillemets simples. Les guillemets simples dans les chaînes sont placés dans un échappement avec deux guillemets simples consécutifs.

Pour analyser une réponse de propriétés JavaScript, un ou plusieurs objets référencés dans la réponse doivent être créés avant le chargement du fichier de propriétés. Voici un exemple d’utilisation de `req=props` pour obtenir la taille de l’image de réponse dans JavaScript :

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
