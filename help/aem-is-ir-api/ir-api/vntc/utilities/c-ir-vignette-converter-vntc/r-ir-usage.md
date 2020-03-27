---
description: Cette rubrique décrit la syntaxe d’utilisation de la technologie virtuelle.
seo-description: Cette rubrique décrit la syntaxe d’utilisation de la technologie virtuelle.
seo-title: Utilisation
solution: Experience Manager
title: Utilisation
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Utilisation{#usage}

Cette rubrique décrit la syntaxe d’utilisation de la technologie virtuelle.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* est le chemin et le nom du fichier à traiter. Peut être un chemin relatif au répertoire de travail actuel ou un chemin absolu. Doit être un fichier de style de vignette, de style d’armoire ou de garniture de fenêtre valide et comporter l’un des suffixes suivants : [!DNL .vnt], [!DNL .vnc]ou [!DNL .vnw]. Obligatoire.

*[!DNL destFile]* est le chemin et le nom du fichier de vignette de sortie. S’il n’est pas spécifié, le fichier de sortie est placé dans le dossier spécifié par `-destpath`. Dans ce scénario, le nom du fichier est généré automatiquement à partir du nom du fichier d’entrée et d’un suffixe de taille, séparés par la chaîne spécifiée par `-separator`. Pour les vignettes, le suffixe de taille correspond à la largeur en pixels de la vignette de sortie à résolution unique, à la largeur du premier d’une vignette de sortie à résolution multiple ou à la valeur &quot;0&quot; en cas de vignette pyramidale. Pour les fichiers de style CAB, la résolution de sortie est utilisée comme suffixe de fichier. *[!DNL destFile]* est ignorée lorsque `-info` est spécifiée.
