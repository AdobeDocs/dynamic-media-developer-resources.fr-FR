---
description: Cette rubrique décrit la syntaxe d’utilisation de la technologie vntc.
seo-description: Cette rubrique décrit la syntaxe d’utilisation de la technologie vntc.
seo-title: Utilisation
solution: Experience Manager
title: Utilisation
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Utilisation{#usage}

Cette rubrique décrit la syntaxe d’utilisation de la technologie vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* est le chemin et le nom du fichier à traiter. Il peut s’agir d’un chemin relatif au répertoire de travail actuel ou d’un chemin absolu. Doit être un fichier de style de vignette, d’armoire ou de fenêtre valide et doit comporter l’un des suffixes suivants : [!DNL .vnt], [!DNL .vnc] ou [!DNL .vnw]. Obligatoire.

*[!DNL destFile]* est le chemin d’accès et le nom du fichier de vignette de sortie. S’il n’est pas spécifié, le fichier de sortie est placé dans le dossier spécifié avec `-destpath`. Dans ce scénario, le nom du fichier est automatiquement généré à partir du nom du fichier d’entrée et d’un suffixe de taille, séparé par la chaîne spécifiée par `-separator`. Pour les vignettes, le suffixe de taille correspond à la largeur en pixels de la vignette de sortie à résolution unique, à la largeur de la première vue d’une vignette de sortie à résolution multiple ou à la largeur de 0 en cas de vignette pyramidale. Pour les fichiers de style d’armoire, la résolution de sortie est utilisée comme suffixe de fichier. *[!DNL destFile]* est ignoré lorsque  `-info` est spécifié.
