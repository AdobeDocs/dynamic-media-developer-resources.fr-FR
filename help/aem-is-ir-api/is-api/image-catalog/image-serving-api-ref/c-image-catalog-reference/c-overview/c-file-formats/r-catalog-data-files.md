---
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini). Elles peuvent être facilement gérées à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.
solution: Experience Manager
title: Fichiers de données de catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Fichiers de données de catalogue{#catalog-data-files}

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini). Elles peuvent être facilement gérées à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.

Essentiellement un tableau à deux dimensions, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et tout nombre d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par des caractères `<TAB>` uniques. Les enregistrements sont séparés par une seule `<CR>` (code ASCII `0xD`), un seul `<LF>` (code ASCII `0xA`) ou une paire `<CR><LF>`.

L’enregistrement de l’en-tête doit contenir les noms exacts pour chaque champ de données. Les champs vides ne sont pas autorisés dans la ligne d’en-tête. Les noms des champs de données ne sont pas sensibles à la casse. Tous les noms de champ doivent être uniques.

Les caractères d’espace ne peuvent pas être utilisés comme séparateurs de champ. Aucun espace n’est autorisé dans l’enregistrement de l’en-tête. Dans les enregistrements de données, tout espace situé au début ou à la fin d’un champ de données est considéré comme faisant partie de ce champ de données.

Dans les enregistrements de données, deux caractères `<TAB>` adjacents indiquent un champ vide. Les champs vides peuvent hériter des valeurs par défaut des attributs du catalogue ou des valeurs par défaut du serveur.

Les champs de données peuvent éventuellement être entourés de guillemets doubles. Ils ne doivent pas contenir de caractères `<CR>`, `<LF>` ou `<TAB>`, sauf si la valeur de données est de type texte et est entourée de guillemets doubles. Les champs de données ne doivent pas être codés en HTTP.

Plusieurs valeurs de données dans le même champ sont séparées par des virgules, sauf indication contraire.

Colonnes dont les noms commencent par &quot;.&quot; sont ignorées. Cela permet de stocker des données dans des catalogues d’images, ce qui n’a aucun intérêt pour le service d’images. Les colonnes dont les noms d’en-tête sont inconnus sont ignorées et un avertissement est écrit dans le fichier journal.

Les noms de champ peuvent être composés de toute combinaison de lettres ASCII, de nombres, ainsi que de &quot;-&quot; et de &quot;_&quot;.

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé apparaît plusieurs fois dans le même fichier de données, l’instance ultérieure l’emporte.
