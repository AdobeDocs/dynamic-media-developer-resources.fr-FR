---
description: Les attributs et champs du catalogue peuvent contenir des données de l’un des types suivants.
solution: Experience Manager
title: Types de données courants
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Types de données courants{#common-data-types}

Les attributs et champs du catalogue peuvent contenir des données de l’un des types suivants.

**Couleur**

Valeur de la couleur. Valeur RVB hexadécimale compressée, éventuellement précédée de 0x. Par exemple, la valeur RVB `128,255,0` peut être spécifiée sous la forme `0x80ff00` ou `80ff00`.

**Indicateur**

`0`=false,  `1`=true, toute autre valeur signifie inconnu ou non spécifié.

**Enum**

0 indique une valeur inconnue ou non spécifiée, comme un champ vide. Les valeurs `enum` valides sont des nombres entiers consécutifs, commençant par 1.

**Nombre entier**

Valeur entière signée (par ex. 0, -12, 34). Les valeurs 0 ou négatives peuvent avoir une signification spéciale.

**Nombre réel**

Valeur à virgule flottante signée (par exemple, `0, 12.5, 245 , -2.34e4`). Les valeurs 0 ou négatives peuvent avoir une signification spéciale.

**Chaîne de texte**

Les délimiteurs de chaîne sont facultatifs, sauf si la chaîne contient des caractères `<CR>`, `<LF>` ou `<TAB>`. Les guillemets simples et doubles peuvent être utilisés comme délimiteurs. Si des guillemets sont utilisés, tout guillemet incorporé dans la chaîne doit être placé dans une séquence d’échappement à l’aide de deux guillemets consécutifs (par ex. &#39; `This month''s Special`&#39;).
