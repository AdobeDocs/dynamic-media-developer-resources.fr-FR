---
description: La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.
solution: Experience Manager
title: Fonction d’impression
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eadcc105-4a86-40f7-867a-3b09a5599a41
TQID: 'https://experienceleague.adobe.com/mbsxiwsrZch87oSFFhXUNp892iQSmfyAFaY7bzDn2MM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# Fonction d’impression{#print-feature}

La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. Cliquer sur le bouton permet à l&#39;utilisateur de choisir une plage d&#39;impression et le nombre de pages par feuille.

La qualité de l’impression peut être ajustée à l’aide du paramètre de configuration `printquality`. Notez qu’il n’est pas recommandé de définir des `printquality` à des valeurs considérablement plus élevées que la valeur par défaut. En effet, cela entraîne une consommation de mémoire très élevée par le navigateur web sur le système du client. Assurez-vous également que la taille maximale de réponse de l’image définie pour votre société Dynamic Media Classic est supérieure à la valeur `printquality` configurée.

>[!NOTE]
>
>La fonction d&#39;impression est disponible uniquement sur les ordinateurs de bureau, à l&#39;exception d&#39;Internet Explorer 9.
