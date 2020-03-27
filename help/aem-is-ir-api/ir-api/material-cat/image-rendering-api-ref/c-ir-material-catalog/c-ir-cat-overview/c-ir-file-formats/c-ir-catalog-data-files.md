---
description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini).
seo-description: Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini).
seo-title: Fichiers de données de catalogue
solution: Experience Manager
title: Fichiers de données de catalogue
topic: Scene7 Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fichiers de données de catalogue{#catalog-data-files}

Les fichiers de données de catalogue peuvent avoir n’importe quel nom et suffixe de fichier (sauf .ini).

Les fichiers de données de catalogue peuvent être conservés facilement à l’aide d’applications prenant en charge les fichiers de données texte délimités par des tabulations, telles que Microsoft Excel et Access.

Essentiellement un tableau bidimensionnel, un fichier de données de catalogue se compose d’un enregistrement d’en-tête qui identifie les colonnes de données et tout nombre d’enregistrements de données (lignes). Les champs des enregistrements d’en-tête et de données sont séparés par des `<TAB>` caractères uniques. Les enregistrements sont séparés par une seule `<CR>` (code ASCII 0xD), une seule `<LF>` (code ASCII 0xA) ou une `<CR><LF>` paire.

L’enregistrement d’en-tête doit contenir les noms exacts de chaque champ de données. Les champs vides ne sont pas autorisés dans la rangée d’en-tête. Les noms des champs de données ne sont pas sensibles à la casse. Tous les noms de champ doivent être uniques.

Aucun espace blanc autre que les séparateurs de `<TAB>` champs n’est autorisé dans les enregistrements d’en-tête et de données.

Dans les enregistrements de données, deux `<TAB>` caractères adjacents indiquent un champ vide. Les champs vides héritent des valeurs par défaut des attributs de catalogue ou des valeurs par défaut du serveur.

Les champs de données ne doivent pas contenir de caractères `<CR>`, `<LF>`ou `<TAB>` , sauf si la valeur de données est de type texte et est entourée de guillemets simples ou. Les champs de données ne doivent pas être codés en HTTP.

Plusieurs valeurs de données dans un même champ sont séparées par des virgules (&#39;,&#39;), sauf indication contraire.

Colonnes dont les noms  avec &quot;.&quot; sont ignorées; cela permet de stocker des données dans des catalogues de matériaux qui ne présentent aucun intérêt pour le rendu d’images. Les colonnes dont le nom d’en-tête est inconnu sont ignorées et un avertissement est écrit dans le fichier journal.

Les noms de champ peuvent être composés de toute combinaison de lettres ASCII, de nombres, de &quot;-&quot; et &quot;_&quot;.

Une ou plusieurs colonnes peuvent être utilisées comme clés d’index. Si la même clé se produit plusieurs fois dans le même fichier de données, l’instance ultérieure prévaut.
