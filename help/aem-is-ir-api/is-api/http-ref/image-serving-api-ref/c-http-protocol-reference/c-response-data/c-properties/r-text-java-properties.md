---
description: Si le texte est spécifié comme format de réponse, les données de réponse sont formatées pour être lisibles en tant que propriétés Java.
solution: Experience Manager
title: Propriétés Text (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Propriétés Text (Java){#text-java-properties}

Si le texte est spécifié comme format de réponse, les données de réponse sont formatées pour être lisibles en tant que propriétés Java.

Une réponse de propriétés de texte standard présente la structure générale suivante :

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne, avant et après le séparateur = . Les valeurs de chaîne peuvent être entourées de guillemets simples ou doubles, mais ils ne sont pas obligatoires.

Les valeurs de chaîne peuvent contenir des caractères d’échappement de style JAVA, tels que `\n`, `\t`, `\:` ou `\\`.
