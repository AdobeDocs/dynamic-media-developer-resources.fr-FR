---
description: Les données de propriété sont renvoyées en réponse aux types req= suivants imageprops et props.
seo-description: Les données de propriété sont renvoyées en réponse aux types req= suivants imageprops et props.
seo-title: Propriétés
solution: Experience Manager
title: Propriétés
topic: Scene7 Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Propriétés{#properties}

Les données de propriété sont renvoyées en réponse aux types req= suivants : imageprops et props.

Les données de réponse sont formatées pour être lisibles en tant que propriétés Java. Une réponse de propriétés de texte type présente la structure générale suivante :

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` peut être vide. L’espace blanc est facultatif au début et à la fin de chaque ligne et avant et après le séparateur &quot;=&quot;. Les valeurs de chaîne peuvent être entourées de guillemets simples ou, mais ils ne sont pas obligatoires.

Les valeurs de chaîne peuvent contenir des caractères d’échappement de style JAVA, tels que \n, \t, \:. ou \\.

**Voir aussi**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
