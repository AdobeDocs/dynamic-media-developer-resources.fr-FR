---
description: Si le texte est spécifié comme format de réponse, les données de réponse sont formatées pour être lisibles en tant que propriétés Java.
solution: Experience Manager
title: Propriétés de texte (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# Propriétés de texte (Java){#text-java-properties}

Si le texte est spécifié comme format de réponse, les données de réponse sont formatées pour être lisibles en tant que propriétés Java.

La structure générale d’une réponse de propriétés de texte type est la suivante :

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

*`propertyValue`* peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne et avant et après le séparateur =. Il est possible d’utiliser des guillemets simples ou doublons pour encadrer les valeurs de chaîne, mais ils ne sont pas obligatoires.

Les valeurs de chaîne peuvent contenir des caractères d’échappement de style JAVA, tels que `\n`, `\t`, `\:` ou `\\`.
