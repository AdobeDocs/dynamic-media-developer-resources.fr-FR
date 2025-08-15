---
title: résoudre
description: Requête de débogage. Cette commande de débogage analyse et prétraite la requête, exécute des recherches de catalogue d’images, des inclusions de modificateur de catalogue, des substitutions de macro et de variable, etc., tout comme req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# résoudre{#resolve}

Requête de débogage. Cette commande de débogage analyse et prétraite la requête, exécute des recherches de catalogue d’images, des inclusions catalog::Modifier, des substitutions de macro et de variable, etc., tout comme req=img.

`req=resolve`

La dernière chaîne de requête est renvoyée, à la place de l’image obtenue, avec le type MIME `text/plain`.

La réponse HTTP ne peut pas être mise en cache.
