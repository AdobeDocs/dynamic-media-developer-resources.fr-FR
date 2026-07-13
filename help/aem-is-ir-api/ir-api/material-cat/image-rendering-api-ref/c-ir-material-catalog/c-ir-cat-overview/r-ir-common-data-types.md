---
title: Types de données courants
description: Les attributs et champs de catalogue peuvent contenir des données de l’un des types suivants.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 162
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

