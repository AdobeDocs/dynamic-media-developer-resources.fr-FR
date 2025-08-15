---
title: Types de données courants
description: Les attributs et champs de catalogue peuvent contenir des données de l’un des types suivants.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Types de données courants{#common-data-types}

Les attributs et champs de catalogue peuvent contenir des données de l’un des types suivants.

**Couleur**

Valeur de la couleur. Valeur RGB hexadécimale compressée, éventuellement précédée de 0x. Par exemple, la valeur RGB `128,255,0` peut être spécifiée comme `0x80ff00` ou `80ff00`.

**Indicateur**

`0`=false, `1`=true, toute autre valeur signifie inconnu ou non spécifié.

**Enum**

`0` indique une valeur inconnue ou non spécifiée, identique à un champ vide. Les valeurs `enum` valides sont des nombres entiers consécutifs commençant par 1.

**Nombre entier**

Valeur entière signée (par exemple, `0, -12, 34`). Les valeurs `0` ou négatives peuvent avoir une signification spéciale.

**Nombre réel**

Valeur à virgule flottante signée (par exemple, `0, 12.5, 245 , -2.34e4`). Les valeurs 0 ou négatives peuvent avoir une signification spéciale.

**Chaîne de texte**

Les délimiteurs de chaîne sont facultatifs, sauf si la chaîne contient des caractères `<CR>`, `<LF>` ou `<TAB>`. Vous pouvez utiliser des guillemets simples et doubles comme délimiteurs. Si des guillemets sont utilisés, tout guillemet incorporé dans la chaîne doit être placé dans une séquence d’échappement en utilisant deux guillemets consécutifs (par exemple, « `This month''s Special` »).
