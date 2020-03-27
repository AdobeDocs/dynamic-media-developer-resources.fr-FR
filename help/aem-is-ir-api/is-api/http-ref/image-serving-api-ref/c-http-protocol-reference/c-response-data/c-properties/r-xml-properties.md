---
description: Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d’un XML qui peut être analysé par n’importe quel analyseur XML standard.
seo-description: Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d’un XML qui peut être analysé par n’importe quel analyseur XML standard.
seo-title: Propriétés XML
solution: Experience Manager
title: Propriétés XML
topic: Scene7 Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Propriétés XML{#xml-properties}

Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d’un XML qui peut être analysé par n’importe quel analyseur XML standard.

Un de réponse de propriétés type a la structure générale suivante :

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

L’ `<prop-group>` élément est utilisé comme  de l’extérieur et pour regrouper les propriétés. Si un groupe est nommé, son nom correspond au nom de l’objet Java/JavaScript.

>[!NOTE]
>
>Le codage de caractères peut être spécifié pour certains `req=` types. Consultez la description de la `req=`commande spécifique pour plus de détails.

