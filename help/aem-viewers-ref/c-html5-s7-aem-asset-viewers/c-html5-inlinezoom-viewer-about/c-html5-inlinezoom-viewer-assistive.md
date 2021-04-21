---
description: Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
title: Assistance technique
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom,Accessibility
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a les attributs de rôle `region` et `aria-label` définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

La vue principale a le rôle `application`. Une brève description de la vue principale est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant principal de vue correspondant. Les conseils de navigation des utilisateurs du clavier sont fournis à l’aide de `aria-describedby`, le texte du conseil d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’un fichier, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les composants qui affichent des échantillons ont le rôle `listbox` avec l&#39;attribut `aria-label` défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les nuances individuelles ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position des nuances dans l’ensemble. Si une nuance est sélectionnée, elle obtient l&#39;attribut `aria-selected` défini sur `true`.
