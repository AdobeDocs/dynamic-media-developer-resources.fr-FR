---
description: Cette rubrique décrit la syntaxe de l’utilisation du protocole vntc.
solution: Experience Manager
title: Utilisation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# Utilisation{#usage}

Cette rubrique décrit la syntaxe de l’utilisation du protocole vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* est le chemin et le nom du fichier à traiter. Il peut s’agir d’un chemin d’accès relatif au répertoire de travail actuel ou d’un chemin d’accès absolu. Doit être un fichier de style de vignette, de style de cabinet ou de fenêtre valide et avoir l’un de ces suffixes : [!DNL .vnt], [!DNL .vnc] ou [!DNL .vnw]. Obligatoire.

*[!DNL destFile]* est le chemin et le nom du fichier de vignette de sortie. S’il n’est pas spécifié, le fichier de sortie est placé dans le dossier spécifié par `-destpath`. Dans ce scénario, le nom de fichier est généré automatiquement à partir du nom du fichier d’entrée et d’un suffixe de taille, séparés par la chaîne spécifiée avec `-separator`. Pour les vignettes, le suffixe de taille est la largeur en pixels de la vignette de sortie à résolution unique, la largeur de la première vue d’une vignette de sortie à résolution multiple ou &quot;0&quot; en cas de vignette pyramidale. Pour les fichiers de style Cabinet, la résolution de sortie est utilisée comme suffixe de fichier. *[!DNL destFile]* est ignoré lorsque  `-info` est spécifié.
