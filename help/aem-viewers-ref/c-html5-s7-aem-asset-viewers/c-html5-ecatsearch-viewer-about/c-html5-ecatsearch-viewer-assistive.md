---
description: Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Prise en charge des technologies d’assistance
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,User
exl-id: fbfc9415-6ab8-466c-9a1f-d33565eff2a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur comporte un `region` de rôle et `aria-label`’attribut défini par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons comportent la `button` de rôle et le texte descriptif définis avec l’attribut `aria-label`. La valeur de `aria-label`’attribut est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, l’attribut `aria-disabled` est défini en conséquence.

La vue principale comporte des `application` de rôle. Une brève description de la vue principale est fournie en `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant de vue principale correspondant. Les conseils de navigation pour les utilisateurs d’un clavier sont fournis à l’aide de `aria-describedby`. Le texte du conseil d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’une ressource, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, les régions et les zones cliquables comportent l’`button` de rôle et le texte descriptif définis avec `aria-label` attribut , avec la valeur du libellé de la zone réactive ou de la zone cliquable. Lorsque l’utilisateur met l’accent sur des zones réactives ou des zones cliquables, des indications de navigation pour les utilisateurs d’un clavier sont fournies à l’aide de `aria-describedby`, le texte de l’indication d’utilisation provenant du symbole de localisation `USAGE_HINT`.

Les miniatures ont le rôle `dialog` avec `aria-label` attribut contrôlé par le symbole de localisation `ThumbnailGridView.LABEL`. Les miniatures individuelles ont des `button` de rôle. Si une miniature est sélectionnée, `aria-selected`’attribut est défini sur `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` avec `aria-label` attribut défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les échantillons individuels ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position de l’échantillon dans l’ensemble. Si une nuance est sélectionnée, l’attribut `aria-selected` est défini sur `true`.

Les listes déroulantes sont activées par des boutons avec un attribut `aria-haspopup` supplémentaire défini sur `true` et l’attribut `aria-controls` faisant référence à l’élément réel du panneau déroulant. Le panneau déroulant lui-même a le rôle `menu` avec les sous-éléments ayant le rôle `menuitem`. Chaque élément de menu possède l’attribut `aria-label` spécifié.

L’interface utilisateur de recherche est regroupée dans l’élément avec le rôle `search`. Le champ de saisie de recherche comporte le `searchbox` de rôle et fait référence au libellé informatif contrôlé par `SearchPanel.INFO_PROMPT` symbole de localisation avec l’attribut `aria-describedby`.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby` .
