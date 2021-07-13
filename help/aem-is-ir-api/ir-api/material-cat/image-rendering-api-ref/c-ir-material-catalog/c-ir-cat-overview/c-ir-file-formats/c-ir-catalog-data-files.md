---
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini).
solution: Experience Manager
title: Fichiers de données de catalogue
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Fichiers de données de catalogue{#catalog-data-files}

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini).

Les fichiers de données de catalogue peuvent être facilement conservés à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.

Essentiellement un tableau à deux dimensions, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et tout nombre d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par des caractères `<TAB>` uniques. Les enregistrements sont séparés par une seule `<CR>` (code ASCII 0xD), une seule `<LF>` (code ASCII 0xA) ou une paire `<CR><LF>`.

L’enregistrement d’en-tête doit contenir les noms exacts pour chaque champ de données. Les champs vides ne sont pas autorisés dans la ligne d’en-tête. Les noms des champs de données ne sont pas sensibles à la casse. Tous les noms de champ doivent être uniques.

Aucun espace blanc autre que les séparateurs de champ `<TAB>` n’est autorisé dans les enregistrements d’en-tête et de données.

Dans les enregistrements de données, deux caractères `<TAB>` adjacents indiquent un champ vide. Les champs vides hériteront des valeurs par défaut des attributs de catalogue ou des valeurs par défaut du serveur.

Les champs de données ne doivent pas contenir de caractères `<CR>`, `<LF>` ou `<TAB>`, sauf si la valeur de données est de type texte et est entourée de guillemets simples ou doubles. Les champs de données ne doivent pas être codés en HTTP.

Plusieurs valeurs de données dans le même champ sont séparées par des virgules (&#39;,&#39;), sauf indication contraire.

Colonnes dont le nom commence par &quot;.&quot; sont ignorées ; cela permet de stocker des données dans des catalogues de matériaux qui ne présentent aucun intérêt pour le rendu d’images. Les colonnes dont les noms d’en-tête sont inconnus sont ignorées et un avertissement est écrit dans le fichier journal.

Les noms de champ peuvent être composés de toute combinaison de lettres ASCII, de nombres, ainsi que de &quot;-&quot; et de &quot;_&quot;.

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé apparaît plusieurs fois dans le même fichier de données, c’est l’instance ultérieure qui prévaudra.
