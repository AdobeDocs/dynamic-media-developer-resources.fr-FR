---
title: Propriétés
description: Les données de propriété sont renvoyées en réponse à req= types imageprops et props.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
TQID: 'https://experienceleague.adobe.com/AIeKRT2-o9Z35SjXjrGECIWHFLRrdJz5JO-CkCOLj8U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# Propriétés{#properties}

Les données de propriété sont renvoyées en réponse aux types req= suivants : imageprops et props.

Les données de réponse sont formatées pour être lisibles en tant que propriétés Java™. Une réponse de propriétés de texte standard possède la structure générale suivante :

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` peut être vide. Les espaces sont facultatifs au début et à la fin de chaque ligne, ainsi qu&#39;avant et après le séparateur « = ». Des guillemets simples ou doubles peuvent être utilisés pour entourer les valeurs de chaîne, mais ils ne sont pas obligatoires.

Les valeurs de chaîne peuvent contenir des caractères d’échappement de style JAVA, tels que `\n`, `\t`, `\:` ou `\\`.

**Voir aussi**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

