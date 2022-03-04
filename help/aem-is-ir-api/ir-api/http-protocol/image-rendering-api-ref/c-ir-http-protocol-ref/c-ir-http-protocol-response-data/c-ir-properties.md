---
title: Propriétés
description: 'Les données de propriété sont renvoyées en réponse aux types req= suivants : imageprops et props.'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# Propriétés{#properties}

Les données de propriété sont renvoyées en réponse aux types req= suivants : Imageprops et props.

Les données de réponse sont formatées pour être lisibles en tant que propriétés Java™. Une réponse de propriétés de texte standard présente la structure générale suivante :

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` Peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne, avant et après le séparateur &quot;=&quot;. Les valeurs de chaîne peuvent être entourées de guillemets simples ou doubles, mais ils ne sont pas obligatoires.

Les valeurs de chaîne peuvent contenir des caractères d’échappement de style JAVA, tels que `\n`, `\t`, `\:`ou `\\`.

**Voir aussi**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
