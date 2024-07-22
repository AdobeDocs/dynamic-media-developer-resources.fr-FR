---
description: Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d'un document XML qui peut être analysé par un analyseur XML standard.
solution: Experience Manager
title: Propriétés XML
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# Propriétés XML{#xml-properties}

Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d&#39;un document XML qui peut être analysé par un analyseur XML standard.

Un document de réponse de propriétés standard présente la structure générale suivante :

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

L’élément `<prop-group>` est utilisé comme conteneur le plus éloigné et pour regrouper les propriétés. Si un groupe est nommé, le nom correspond au nom de l’objet Java/JavaScript.

>[!NOTE]
>
>Le codage des caractères peut être spécifié pour certains types `req=`. Pour plus d&#39;informations, consultez la description de la commande `req=`spécifique.
