---
title: Fichiers de données de catalogue
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Fichiers de données de catalogue{#catalog-data-files}

Les fichiers de données du catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf `.ini`).

Les fichiers de données de catalogue peuvent être facilement conservés à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft® Excel et Access.

Essentiellement un tableau à deux dimensions, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et tout nombre d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par une seule `<TAB>` caractères. Les enregistrements sont séparés par une seule `<CR>` (code ASCII) `0xD`), un seul `<LF>` (code ASCII) `0xA`), ou un `<CR><LF>` paire .

L’enregistrement d’en-tête doit contenir les noms exacts pour chaque champ de données. Les champs vides ne sont pas autorisés dans la ligne d’en-tête. Les noms des champs de données ne sont pas sensibles à la casse. Tous les noms de champ doivent être uniques.

Aucun espace autre que le `<TAB>` les séparateurs de champ sont autorisés dans les enregistrements d’en-tête et de données.

Dans les enregistrements de données, deux enregistrements adjacents `<TAB>` Les caractères indiquent un champ vide. Les champs vides héritent des valeurs par défaut des attributs de catalogue ou des valeurs par défaut du serveur.

Les champs de données ne doivent pas contenir `<CR>`, `<LF>`ou `<TAB>` , sauf si la valeur de données est de type texte et est entourée de guillemets simples ou doubles. Ne codez pas les champs de données par HTTP.

Plusieurs valeurs de données dans le même champ sont séparées par des virgules (&#39;,&#39;), sauf indication contraire.

Colonnes dont le nom commence par &quot;.&quot; sont ignorées ; cela permet de stocker des données dans des catalogues de matériaux qui ne présentent aucun intérêt pour le rendu d’images. Les colonnes dont les noms d’en-tête sont inconnus sont ignorées et un avertissement est écrit dans le fichier journal.

Les noms de champ peuvent être composés de n’importe quelle combinaison de lettres ASCII, de nombres et de &quot;-&quot; et de &quot;_&quot;.

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé apparaît plusieurs fois dans le même fichier de données, l’instance ultérieure l’emporte.
