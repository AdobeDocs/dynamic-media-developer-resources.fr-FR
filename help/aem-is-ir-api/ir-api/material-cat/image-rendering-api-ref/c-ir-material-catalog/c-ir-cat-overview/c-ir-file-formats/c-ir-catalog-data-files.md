---
title: Fichiers de données du catalogue
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (à l’exception de .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Fichiers de données du catalogue{#catalog-data-files}

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf `.ini`).

Les fichiers de données de catalogue peuvent être facilement conservés à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft® Excel et Access.

Essentiellement une table bidimensionnelle, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et un nombre illimité d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par des caractères `<TAB>` uniques. Les enregistrements sont séparés par une seule `<CR>` (`0xD` de code ASCII), une seule `<LF>` (`0xA` de code ASCII) ou une paire de `<CR><LF>`.

L’enregistrement de l’en-tête doit contenir les noms exacts de chaque champ de données. Les champs vides ne sont pas autorisés dans la ligne d’en-tête. Les noms des champs de données ne respectent pas la casse. Tous les noms de champ doivent être uniques.

Aucun espace blanc autre que les séparateurs de champs `<TAB>` n’est autorisé dans les enregistrements d’en-tête et de données.

Dans les enregistrements de données, deux caractères `<TAB>` adjacents indiquent un champ vide. Les champs vides héritent des valeurs par défaut des attributs du catalogue ou des valeurs par défaut du serveur.

Les champs de données ne doivent pas contenir de caractères `<CR>`, `<LF>` ou `<TAB>`, sauf si la valeur de données est de type texte et est entourée de guillemets simples ou doubles. Ne codez pas de champs de données HTTP.

Sauf indication contraire, plusieurs valeurs de données d’un même champ sont séparées par des virgules (’,’).

Colonnes dont le nom commence par « . » sont ignorées ; cela permet de stocker des données dans des catalogues de matériaux qui n’ont aucun intérêt pour le rendu d’images. Les colonnes dont les noms d’en-tête sont inconnus sont ignorées et un avertissement est consigné dans le fichier journal.

Les noms de champ peuvent être constitués de n’importe quelle combinaison de lettres ASCII, de chiffres et de caractères « - » et « _ ».

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé apparaît plusieurs fois dans le même fichier de données, l’instance la plus récente prévaut.
