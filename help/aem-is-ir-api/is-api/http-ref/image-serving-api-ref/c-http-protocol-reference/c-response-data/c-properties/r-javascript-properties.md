---
description: Si JavaScript™ est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées en tant que fichier d’inclusion JavaScript™.
solution: Experience Manager
title: Propriétés JavaScript™
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Propriétés JavaScript™{#javascript-properties}

Si JavaScript™ est spécifié comme format de réponse, les données de réponse sont formatées pour être analysées en tant que fichier d’inclusion JavaScript™.

La structure générale d’une réponse aux propriétés JavaScript™ standard est la suivante :

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

Pour analyser une réponse de propriétés JavaScript™, tout objet ou objet référencé dans la réponse doit être créé avant le chargement du fichier de propriétés. Voici un exemple d’utilisation de `req=props` pour obtenir la taille de l’image de réponse dans JavaScript™ :

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

