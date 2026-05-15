---
title: Propriétés de JavaScript
description: Si JavaScript est spécifié comme format de réponse, les données de réponse sont formatées afin d’être analysées en tant que fichier JavaScript&trade; include.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
TQID: 'https://experienceleague.adobe.com/T6xqUHtT9XX4b9bP-wi-b0dDBe2LHE3vcBcJI6cMKqE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
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
