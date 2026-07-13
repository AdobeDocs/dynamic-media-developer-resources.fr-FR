---
title: Utilisation
description: Cette rubrique décrit la syntaxe d'utilisation de vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 1%

---

# Utilisation{#usage}

Cette rubrique décrit la syntaxe d&#39;utilisation de vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* correspond au chemin d’accès et au nom du fichier à traiter. Il peut s’agir d’un chemin relatif au répertoire de travail actuel ou d’un chemin absolu. Il doit s’agir d’un fichier de style vignette, armoire ou couvre-fenêtre valide et comporter l’un des suffixes suivants :

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Obligatoire.

*[!DNL destFile]* est le chemin d’accès et le nom du fichier de vignette de sortie. S’il n’est pas spécifié, le fichier de sortie est placé dans le dossier spécifié avec `-destpath`. Dans ce scénario, le nom du fichier est automatiquement généré à partir du nom du fichier d’entrée et d’un suffixe de taille, séparés par la chaîne spécifiée par `-separator`. Pour les vignettes, le suffixe de taille est la largeur en pixels de la vignette de sortie à résolution unique, la largeur de la première vue d&#39;une vignette de sortie à résolution multiple ou « 0 » s&#39;il existe une vignette pyramidale. Pour les fichiers de style CAB, la résolution de sortie est utilisée comme suffixe de fichier. *[!DNL destFile]* est ignoré lorsque `-info` est spécifié.

