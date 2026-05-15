---
description: Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d’un document XML qui peut être analysé par n’importe quel analyseur XML standard.
solution: Experience Manager
title: Propriétés XML
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: 'https://experienceleague.adobe.com/Nljy83DDIbeY6l-d6F02NlaFzyCFJny7iesxnF9mFyo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# Propriétés XML{#xml-properties}

Si xml est spécifié comme format de réponse, les données de réponse sont formatées sous la forme d’un document XML qui peut être analysé par n’importe quel analyseur XML standard.

Un document de réponse de propriétés standard possède la structure générale suivante :

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

L’élément `<prop-group>` est utilisé comme conteneur le plus à l’extérieur et pour les propriétés de regroupement. Si un groupe est nommé , le nom correspond au nom de l’objet Java/JavaScript.

>[!NOTE]
>
>L’encodage des caractères peut être spécifié pour certains types de `req=`. Reportez-vous à la description de la commande `req=` spécifique pour plus d’informations.
