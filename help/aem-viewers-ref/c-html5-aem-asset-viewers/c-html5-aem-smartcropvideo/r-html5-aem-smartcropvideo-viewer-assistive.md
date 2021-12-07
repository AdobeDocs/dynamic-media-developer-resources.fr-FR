---
title: Prise en charge des technologies d’assistance
description: Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video,Accessibility
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration aux technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur a un rôle `region` et `aria-label` définie par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé à l’aide de la fonction `Container.LABEL` symbole de localisation.

Les boutons ont un rôle `button` et texte descriptif avec `aria-label` attribut. La valeur de `aria-label` est renseigné à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` est défini en conséquence.

Les composants de curseur ont un rôle `slider` avec des attributs `aria-valuenow`, `aria-valuemin`, et `aria-valuemax` pour décrire la position actuelle du curseur.

Les listes déroulantes sont activées par des boutons avec des `aria-haspopup` définie sur `true` et `aria-controls` faisant référence à l’élément de panneau déroulant réel. Le panneau déroulant lui-même a le rôle `menu` avec des sous-éléments ayant un rôle `menuitem`. Chaque élément de menu comporte la variable `aria-label` spécifié.

Les boîtes de dialogue modales ont un rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par le `aria-labelledby` attribut.
