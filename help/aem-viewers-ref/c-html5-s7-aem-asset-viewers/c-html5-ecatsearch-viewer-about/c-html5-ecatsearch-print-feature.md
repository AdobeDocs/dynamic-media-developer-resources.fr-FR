---
description: La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.
solution: Experience Manager
title: Fonction d’impression
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Fonction d’impression{#print-feature}

La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. Cliquer sur le bouton permet à l&#39;utilisateur de choisir une plage d&#39;impression et le nombre de pages par feuille.

La qualité de l&#39;impression peut être ajustée à l&#39;aide du paramètre de configuration `printquality`. Notez que la définition de `printquality` sur des valeurs significativement plus élevées que la valeur par défaut n’est pas recommandée. Cela est dû au fait que le navigateur web consomme beaucoup de mémoire sur le système du client. Assurez-vous également que la taille maximale de réponse de l’image définie pour votre société Dynamic Media Classic est supérieure à la valeur `printquality` configurée.

>[!NOTE]
>
>La fonction d’impression n’est disponible que sur les ordinateurs de bureau, à l’exception d’Internet Explorer 9.
