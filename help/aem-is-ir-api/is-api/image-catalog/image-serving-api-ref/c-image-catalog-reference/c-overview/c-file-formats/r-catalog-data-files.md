---
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (à l’exception de .ini). Ils peuvent être facilement conservés à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.
solution: Experience Manager
title: Fichiers de données du catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
TQID: 'https://experienceleague.adobe.com/h4-MIosWMEWhmbAYbpS9xm22nDzEPO6APGEezCA1B-Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 0%

---

# Fichiers de données du catalogue{#catalog-data-files}

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (à l’exception de .ini). Ils peuvent être facilement conservés à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.

Il s’agit essentiellement d’un tableau à deux dimensions, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et un nombre illimité d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par des caractères `<TAB>` uniques. Les enregistrements sont séparés par une seule `<CR>` (`0xD` de code ASCII), une seule `<LF>` (`0xA` de code ASCII) ou une paire de `<CR><LF>`.

L’enregistrement de l’en-tête doit contenir les noms exacts de chaque champ de données. Les champs vides ne sont pas autorisés dans la ligne d’en-tête. Les noms des champs de données ne respectent pas la casse. Tous les noms de champ doivent être uniques.

Les espaces ne peuvent pas être utilisés comme séparateurs de champs. Aucun espace n’est autorisé dans l’enregistrement d’en-tête. Dans les enregistrements de données, tout espace au début ou à la fin d’un champ de données est considéré comme faisant partie de ce champ de données.

Dans les enregistrements de données, deux caractères `<TAB>` adjacents indiquent un champ vide. Les champs vides peuvent hériter des valeurs par défaut des attributs du catalogue ou des valeurs par défaut du serveur.

Les champs de données peuvent éventuellement être entourés de guillemets doubles. Ils ne doivent pas contenir de caractères `<CR>`, `<LF>` ou `<TAB>`, sauf si la valeur de données est de type texte et est entourée de guillemets doubles. Les champs de données ne doivent pas être codés en HTTP.

Sauf indication contraire, plusieurs valeurs de données d’un même champ sont séparées par des virgules.

Colonnes dont le nom commence par « . » sont ignorées. Cela permet de stocker des données dans des catalogues d’images, ce qui n’intéresse pas la diffusion d’images. Les colonnes dont les noms d’en-tête sont inconnus sont ignorées et un avertissement est consigné dans le fichier journal.

Les noms de champ peuvent être constitués de toute combinaison de lettres ASCII, de chiffres, ainsi que de « - » et « _ ».

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé apparaît plusieurs fois dans le même fichier de données, l’instance la plus récente prévaut.
