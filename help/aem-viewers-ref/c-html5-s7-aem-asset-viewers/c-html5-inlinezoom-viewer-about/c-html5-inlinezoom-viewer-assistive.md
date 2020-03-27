---
description: Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
seo-description: Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
seo-title: Prise en charge des technologies d'assistance
solution: Experience Manager
title: Prise en charge des technologies d'assistance
topic: Dynamic media
uuid: 9de323c9-d383-41e9-ae44-06600f44a85e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Prise en charge des technologies d&#39;assistance{#assistive-technology-support}

Tous les composants du lecteur prennent en charge les rôles et les attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de lecteur de niveau supérieur a un rôle `region` `aria-label` et un attribut définis par défaut sur le nom de la visionneuse. Vous pouvez contrôler l’étiquette à l’aide du `Container.LABEL` symbole .

Le principal a un rôle `application`. Une brève description de la  principale du est fournie dans `aria-roledescription`, avec la valeur définie par le symbole de la  de du composant `ROLE_DESCRIPTION` principal de l&#39;ensemble de l&#39;ensemble. Les conseils de navigation pour les utilisateurs du clavier sont fournis à l’aide `aria-describedby`, le texte du conseil d’utilisation provient du symbole `USAGE_HINT` . Si un libellé est défini dans le champ UserData d’un fichier, l’ `aria-label` attribut est défini avec la valeur de ce libellé.

Les composants qui affichent des échantillons ont le rôle `listbox` dont l’attribut `aria-label` est défini sur la valeur du symbole de  de `LABEL` de ce composant. Les nuances individuelles ont le rôle `option` avec `aria-setsize` `aria-posinset` et les attributs pour décrire la position des nuances dans la visionneuse. Si une nuance est sélectionnée, l’ `aria-selected` attribut est défini sur `true`.
