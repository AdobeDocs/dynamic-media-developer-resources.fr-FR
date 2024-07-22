---
title: Types de données courants
description: Les attributs et champs du catalogue peuvent contenir des données de l’un des types suivants.
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

Les attributs et champs du catalogue peuvent contenir des données de l’un des types suivants.

**Color**

Valeur de la couleur. Valeur RGB hexadécimale bondée, éventuellement précédée de 0x. Par exemple, la valeur du RGB `128,255,0` peut être spécifiée sous la forme `0x80ff00` ou `80ff00`.

**Flag**

`0`=false, `1`=true, toute autre valeur signifie inconnu ou non spécifié.

**Enum**

`0` indique une valeur inconnue ou non spécifiée, comme un champ vide. Les valeurs `enum` valides sont des nombres entiers consécutifs, commençant par 1.

**Nombre entier**

Valeur entière signée (par exemple `0, -12, 34`). `0` ou des valeurs négatives peuvent avoir une signification spéciale.

**Nombre réel**

Valeur en virgule flottante signée (par exemple, `0, 12.5, 245 , -2.34e4`). Les valeurs 0 ou négatives peuvent avoir une signification spéciale.

**Chaîne de texte**

Les délimiteurs de chaîne sont facultatifs, sauf si la chaîne contient des caractères `<CR>`, `<LF>` ou `<TAB>`. Les guillemets simples et doubles peuvent être utilisés comme délimiteurs. Si des guillemets sont utilisés, tout guillemet incorporé dans la chaîne doit être placé dans une séquence d’échappement à l’aide de deux guillemets consécutifs (par exemple, &#39; `This month''s Special`&#39;).
