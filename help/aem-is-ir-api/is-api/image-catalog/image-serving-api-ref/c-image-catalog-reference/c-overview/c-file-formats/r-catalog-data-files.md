---
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini). Ils peuvent être conservés facilement à l'aide d'applications prenant en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.
solution: Experience Manager
title: Fichiers de données de catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Fichiers de données de catalogue{#catalog-data-files}

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini). Ils peuvent être conservés facilement à l&#39;aide d&#39;applications prenant en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.

Essentiellement un tableau bidimensionnel, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et tout nombre d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par des caractères `<TAB>` uniques. Les enregistrements sont séparés par une seule `<CR>` (code ASCII `0xD`), une seule `<LF>` (code ASCII `0xA`) ou une paire `<CR><LF>`.

L’enregistrement d’en-tête doit contenir les noms exacts de chaque champ de données. Les champs vides ne sont pas autorisés dans la rangée d’en-tête. Les noms des champs de données ne sont pas sensibles à la casse. Tous les noms de champ doivent être uniques.

Les caractères d’espace ne peuvent pas être utilisés comme séparateurs de champ. Aucun espace n’est autorisé dans l’enregistrement d’en-tête. Dans les enregistrements de données, les espaces situés au début ou à la fin d’un champ de données sont considérés comme faisant partie de ce champ de données.

Dans les enregistrements de données, deux caractères `<TAB>` adjacents indiquent un champ vide. Les champs vides peuvent hériter des valeurs par défaut des attributs de catalogue ou des valeurs par défaut du serveur.

Les champs de données peuvent éventuellement être entourés de guillemets de doublon. Ils ne doivent pas contenir de caractères `<CR>`, `<LF>` ou `<TAB>`, sauf si la valeur de données est de type texte et est entourée de guillemets de doublon. Les champs de données ne doivent pas être encodés en HTTP.

Plusieurs valeurs de données dans un même champ sont séparées par des virgules, sauf indication contraire.

Colonnes dont les noms sont débuts de &quot;&quot;. sont ignorées. Cela permet de stocker des données dans des catalogues d’images, ce qui ne présente aucun intérêt pour la diffusion d’images. Les colonnes dont le nom d’en-tête est inconnu sont ignorées et un avertissement est écrit dans le fichier journal.

Les noms de champ peuvent être composés de toute combinaison de lettres ASCII, de chiffres, ainsi que de &quot;-&quot; et &quot;_&quot;.

Une ou plusieurs colonnes peuvent être utilisées comme clés d&#39;index. Si la même clé apparaît plusieurs fois dans le même fichier de données, l’instance ultérieure prévaut.
