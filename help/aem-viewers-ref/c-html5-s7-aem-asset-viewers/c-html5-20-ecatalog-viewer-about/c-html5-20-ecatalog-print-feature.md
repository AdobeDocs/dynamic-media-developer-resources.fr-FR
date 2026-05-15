---
title: Fonction d’impression
description: La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
TQID: 'https://experienceleague.adobe.com/5eIB7D6O7-d8prjO0MJ9PzUU9TPQe7SZcZAEtznPsv4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# Fonction d’impression{#print-feature}

La visionneuse vous permet de générer le contenu du catalogue sur une imprimante.

La fonction d’impression est déclenchée par un bouton dédié dans la barre d’outils. Cliquer sur le bouton permet à l&#39;utilisateur de choisir une plage d&#39;impression et le nombre de pages par feuille.

La qualité de l’impression peut être ajustée à l’aide du paramètre de configuration `printquality`. Il n’est pas recommandé de définir des valeurs `printquality` supérieures à la valeur par défaut. En effet, cela entraîne une consommation de mémoire élevée par le navigateur web sur le système du client. Assurez-vous également que la taille maximale de réponse de l’image définie pour votre société Dynamic Media Classic est supérieure à la valeur `printquality` configurée.

>[!NOTE]
>
>La fonction d&#39;impression est disponible uniquement sur les ordinateurs de bureau, à l&#39;exception d&#39;Internet Explorer 9.
