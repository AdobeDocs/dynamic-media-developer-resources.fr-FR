---
description: Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Assistance technique
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,Business Practitioner
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a les attributs de rôle `region` et `aria-label` définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons ont le rôle `button` et un texte descriptif défini avec l&#39;attribut `aria-label`. La valeur de l’attribut `aria-label` est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, l’attribut `aria-disabled` est défini en conséquence.

Les composants du curseur ont le rôle `slider` avec des attributs `aria-valuenow`, `aria-valuemin` et `aria-valuemax` pour décrire la position actuelle du curseur.

Les miniatures ont le rôle `dialog` avec l&#39;attribut `aria-label` contrôlé par le symbole de localisation `ThumbnailGridView.LABEL`. Les miniatures individuelles ont un rôle `button`. Si une miniature est sélectionnée, elle obtient l’attribut `aria-selected` défini sur `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` avec l&#39;attribut `aria-label` défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les nuances individuelles ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position des nuances dans l’ensemble. Si une nuance est sélectionnée, elle obtient l&#39;attribut `aria-selected` défini sur `true`.

Les listes déroulantes sont activées par des boutons avec des attributs `aria-haspopup` supplémentaires définis sur `true` et `aria-controls` qui référencent l’élément de panneau déroulant réel. Le panneau déroulant a lui-même le rôle `menu` avec des sous-éléments ayant le rôle `menuitem`. L&#39;attribut `aria-label` est spécifié pour chaque élément de menu.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby`.
