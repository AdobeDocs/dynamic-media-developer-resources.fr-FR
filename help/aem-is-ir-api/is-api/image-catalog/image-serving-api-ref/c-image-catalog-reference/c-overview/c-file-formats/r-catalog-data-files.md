---
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe (à l’exception .ini). Ils peuvent être maintenus facilement à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, tels que Microsoft Excel et Access.
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

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (à l’exception de .ini). Ils peuvent être facilement conservés à l’aide d’applications qui prennent en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.

Essentiellement un tableau bidimensionnel, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et n’importe quel nombre d’enregistrements de données (lignes). Les champs de l’en-tête et des enregistrements de données sont séparés par des caractères uniques `<TAB>` . Les enregistrements sont séparés par un seul `<CR>` (code ASCII), un seul `0xD` (code `<LF>` `0xA`ASCII) ou une `<CR><LF>` paire.

L’enregistrement d’en-tête doit contenir les noms exacts de chaque champ de données. Les champs vides ne sont pas autorisés dans la rangée d’en-tête. Les noms des champs de données ne sont pas sensibles à la casse. Tous les noms de champs doivent être uniques.

Les espaces ne peuvent pas être utilisés comme séparateurs de champs. Aucun espace n’est autorisé dans l’enregistrement d’en-tête. Dans les enregistrements de données, tous les espaces au début ou à la fin d’un champ de données sont considérés comme faisant partie de ce champ de données.

Dans les enregistrements de données, deux caractères adjacents `<TAB>` indiquent un champ vide. Les champs vides peuvent hériter des valeurs par défaut des attributs de catalogue ou des valeurs par défaut du serveur.

Les champs de données peuvent éventuellement être encadrés de guillemets doubles. Ils ne doivent pas contenir `<CR>` `<LF>`, ni `<TAB>` caractères, sauf si la valeur de données est de type texte et est entourée de guillemets doubles. Les champs de données ne doivent pas être codés en HTTP.

Sauf indication contraire, plusieurs valeurs de données d’un même champ sont séparées par des virgules.

Les colonnes dont le nom commence par « . » sont ignorées. Cela permet de stocker des données dans des catalogues d’images, ce qui n’a aucun intérêt pour Image Server. Les colonnes dont le nom d’en-tête est inconnu sont ignorées et un avertissement est écrit dans le fichier journal.

Les noms de champ peuvent être constitués de n’importe quelle combinaison de lettres ASCII, de chiffres, ainsi que de « - » et « _ ».

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé apparaît plusieurs fois dans le même fichier de données, c’est la dernière instance qui prévaut.
