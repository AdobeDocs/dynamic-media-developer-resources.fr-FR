---
description: Cette rubrique décrit la syntaxe d’utilisation de la technologie vntc.
solution: Experience Manager
title: Utilisation
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Utilisation{#usage}

Cette rubrique décrit la syntaxe d’utilisation de la technologie vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* est le chemin et le nom du fichier à traiter. Il peut s’agir d’un chemin relatif au répertoire de travail actuel ou d’un chemin absolu. Doit être un fichier de style de vignette, d’armoire ou de fenêtre valide et doit comporter l’un des suffixes suivants : [!DNL .vnt], [!DNL .vnc] ou [!DNL .vnw]. Obligatoire.

*[!DNL destFile]* est le chemin d’accès et le nom du fichier de vignette de sortie. S’il n’est pas spécifié, le fichier de sortie est placé dans le dossier spécifié avec `-destpath`. Dans ce scénario, le nom du fichier est automatiquement généré à partir du nom du fichier d’entrée et d’un suffixe de taille, séparé par la chaîne spécifiée par `-separator`. Pour les vignettes, le suffixe de taille correspond à la largeur en pixels de la vignette de sortie à résolution unique, à la largeur de la première vue d’une vignette de sortie à résolution multiple ou à la largeur de 0 en cas de vignette pyramidale. Pour les fichiers de style d’armoire, la résolution de sortie est utilisée comme suffixe de fichier. *[!DNL destFile]* est ignoré lorsque  `-info` est spécifié.
