---
title: Soutien aux technologies d’assistance
description: Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos,Accessibility
role: Developer,User
exl-id: 3d9f6389-e73c-4d31-a7c1-b321f065ce8c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Soutien aux technologies d’assistance{#assistive-technology-support}

Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) pour améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

Le rôle `region` et `aria-label` l’attribut de l’élément visionneuse de niveau supérieur sont définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler l’étiquette avec le symbole de `Container.LABEL` localisation.

Le rôle `button` et le texte descriptif des boutons sont définis avec `aria-label` l’attribut. La valeur d’attribut `aria-label` est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` l’attribut est défini en conséquence.

Les composants curseurs ont le rôle `slider` avec les attributs `aria-valuenow`, `aria-valuemin`et `aria-valuemax` pour décrire la position actuelle du curseur.

Les miniatures ont le rôle `dialog` avec `aria-label` attribut contrôlé par le symbole de `ThumbnailGridView.LABEL` localisation. Les miniatures individuelles ont un rôle `button`. Si une vignette est sélectionnée, l’attribut est `aria-selected` défini sur `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` avec `aria-label` l’attribut défini sur la valeur du symbole de `LABEL` localisation de ce composant. Les échantillons individuels ont le rôle `option` `aria-setsize` et `aria-posinset` les attributs nécessaires pour décrire la position de l’échantillon dans l’ensemble. Si un échantillon est sélectionné, l’attribut `aria-selected` est défini sur `true`.

Les listes déroulantes sont activées par des boutons avec l’attribut supplémentaire `aria-haspopup` défini sur `true` et `aria-controls` l’attribut référençant l’élément de panneau déroulant réel. Le panneau déroulant a lui-même le rôle et les sous-éléments ont le rôle `menu` `menuitem`. L’attribut `aria-label` spécifié est attribué pour chaque élément de menu.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby` .
