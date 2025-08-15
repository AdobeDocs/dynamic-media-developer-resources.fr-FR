---
title: Prise en charge des technologies d’assistance
description: Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video,Accessibility
role: Developer,User
exl-id: 0d6bc444-a4c2-47e4-b408-a6df85ebff72
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur comporte un `region` de rôle et `aria-label`’attribut défini par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons comportent la `button` de rôle et le texte descriptif définis avec l’attribut `aria-label`. La valeur de `aria-label`’attribut est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` attribut est défini en conséquence.

Les composants curseur ont le rôle `slider` avec les attributs `aria-valuenow`, `aria-valuemin` et `aria-valuemax` pour décrire la position actuelle du curseur.

Les listes déroulantes sont activées par des boutons avec un attribut `aria-haspopup` supplémentaire défini sur `true` et un attribut `aria-controls` faisant référence à l’élément réel du panneau déroulant. Le panneau déroulant lui-même dispose du rôle `menu` avec les sous-éléments dont le rôle est `menuitem`. Chaque élément de menu possède l’attribut `aria-label` spécifié.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby` .
