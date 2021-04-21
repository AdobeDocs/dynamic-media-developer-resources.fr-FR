---
description: Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Assistance technique
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search,Accessibility
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a les attributs de rôle `region` et `aria-label` définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons ont le rôle `button` et un texte descriptif défini avec l&#39;attribut `aria-label`. La valeur de l’attribut `aria-label` est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, l’attribut `aria-disabled` est défini en conséquence.

La vue principale a le rôle `application`. Une brève description de la vue principale est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant principal de vue correspondant. Les conseils de navigation des utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte du conseil d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’un fichier, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les zones réactives, les régions et les zones cliquables ont le rôle `button` et un texte descriptif défini avec l’attribut `aria-label`, avec la valeur de la zone réactive ou du libellé de zone cliquable. Lorsque l’utilisateur met l’accent sur les zones réactives ou les zones cliquables, des conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte du conseil d’utilisation provenant du symbole de localisation `USAGE_HINT`.

Les miniatures ont le rôle `dialog` avec l&#39;attribut `aria-label` contrôlé par le symbole de localisation `ThumbnailGridView.LABEL`. Les miniatures individuelles ont un rôle `button`. Si une miniature est sélectionnée, elle obtient l’attribut `aria-selected` défini sur `true`.

Les composants qui affichent des échantillons ont le rôle `listbox` avec l&#39;attribut `aria-label` défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les nuances individuelles ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position des nuances dans l’ensemble. Si une nuance est sélectionnée, elle obtient l&#39;attribut `aria-selected` défini sur `true`.

Les listes déroulantes sont activées par des boutons avec un attribut `aria-haspopup` supplémentaire défini sur `true` et l&#39;attribut `aria-controls` référençant l&#39;élément de panneau déroulant réel. Le panneau déroulant a lui-même le rôle `menu` avec des sous-éléments ayant le rôle `menuitem`. L&#39;attribut `aria-label` est spécifié pour chaque élément de menu.

L&#39;interface utilisateur de recherche est regroupée dans l&#39;élément avec le rôle `search`. Le champ d&#39;entrée de recherche a le rôle `searchbox` et référence le libellé informatif contrôlé par le symbole de localisation `SearchPanel.INFO_PROMPT` avec l&#39;attribut `aria-describedby`.

Les boîtes de dialogue modales ont le rôle `dialog`. L’élément d’en-tête de la boîte de dialogue est référencé par l’attribut `aria-labelledby`.
