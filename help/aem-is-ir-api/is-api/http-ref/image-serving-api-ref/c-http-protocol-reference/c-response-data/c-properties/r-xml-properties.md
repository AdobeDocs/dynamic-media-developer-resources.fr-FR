---
description: Si xml est spécifié comme format de réponse, les données de réponse sont formatées en document XML qui peut être analysé par n’importe quel analyseur XML standard.
solution: Experience Manager
title: Propriétés XML
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# Propriétés XML{#xml-properties}

Si xml est spécifié comme format de réponse, les données de réponse sont formatées en document XML qui peut être analysé par n’importe quel analyseur XML standard.

Un document de réponse de propriétés type présente la structure générale suivante :

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

L&#39;élément `<prop-group>` est utilisé comme conteneur le plus à l&#39;extérieur et pour regrouper les propriétés. Si un groupe est nommé, le nom correspond au nom de l’objet Java/JavaScript.

>[!NOTE]
>
>L&#39;encodage des caractères peut être spécifié pour certains types `req=`. Consultez la description de la commande `req=`spécifique pour plus de détails.

