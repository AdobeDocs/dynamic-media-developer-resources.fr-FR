---
description: Les données de propriété sont renvoyées en réponse aux types req= suivants imageprops et props.
solution: Experience Manager
title: Propriétés
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---


# Propriétés{#properties}

Les données de propriété sont renvoyées en réponse aux types req= suivants : imageprops et props.

Les données de réponse sont formatées pour être lisibles en tant que propriétés Java. La structure générale d’une réponse de propriétés de texte type est la suivante :

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne et avant et après le séparateur &quot;=&quot;. Il est possible d’utiliser des guillemets simples ou doublons pour encadrer les valeurs de chaîne, mais ils ne sont pas obligatoires.

Les valeurs de chaîne peuvent contenir des caractères d’échappement de style JAVA, tels que `\n`, `\t`, `\:`. ou `\\`.

**Voir aussi**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
