---
description: Les attributs et les champs du catalogue peuvent contenir des données de l’un des types suivants.
seo-description: Les attributs et les champs du catalogue peuvent contenir des données de l’un des types suivants.
seo-title: Types de données courants
solution: Experience Manager
title: Types de données courants
topic: Scene7 Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Types de données courants{#common-data-types}

Les attributs et les champs du catalogue peuvent contenir des données de l’un des types suivants.

**Couleur**

Valeur de couleur. Valeur RVB compressée hexadécimale, éventuellement précédée de 0x. Par exemple, la valeur RVB `128,255,0` peut être spécifiée comme `0x80ff00` ou `80ff00`.

**Indicateur**

`0`=false, `1`=true, toute autre valeur signifie inconnu ou non spécifié.

**Enum**

0 indique une valeur inconnue ou non spécifiée, comme un champ vide. Les `enum` valeurs valides sont des nombres entiers consécutifs, commençant par 1.

**Nombre entier**

Valeur entière signée (ex. : 0, -12, 34). Les valeurs 0 ou négatives peuvent avoir une signification spéciale.

**Nombre réel**

Valeur en virgule flottante signée (ex. `0, 12.5, 245 , -2.34e4`). Les valeurs 0 ou négatives peuvent avoir une signification spéciale.

**Chaîne de texte**

Les délimiteurs de chaîne sont facultatifs, sauf si la chaîne contient des caractères `<CR>`, `<LF>`ou `<TAB>` . Les guillemets simples et peuvent être utilisés comme délimiteurs. Si des guillemets sont utilisés, ces guillemets incorporés dans la chaîne doivent être placés en séquence d’échappement à l’aide de deux guillemets consécutifs (p. ex. &#39; `This month''s Special`&#39;).
