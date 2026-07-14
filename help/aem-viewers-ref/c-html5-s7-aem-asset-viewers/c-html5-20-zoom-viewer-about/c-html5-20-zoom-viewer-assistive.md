---
title: Prise en charge des technologies d’assistance
description: Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom,Accessibility
role: Developer,User
exl-id: ef2cf58a-bdf0-4136-8d91-692c899cfef7
TQID: 'https://experienceleague.adobe.com/WlB-9svy0pfy2yIcqal02uL3m9QzLzYtVh4X4f5TwAs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Prise en charge des technologies d’assistance{#assistive-technology-support}

Tous les composants de la visionneuse prennent en charge les rôles et attributs ARIA (Accessible Rich Internet Applications) afin d’améliorer l’intégration avec les technologies d’assistance telles que les lecteurs d’écran.

L’élément de visionneuse de niveau supérieur comporte un `region` de rôle et `aria-label`’attribut défini par défaut sur le nom de la visionneuse. Vous pouvez contrôler le libellé avec le symbole de localisation `Container.LABEL`.

Les boutons comportent la `button` de rôle et le texte descriptif définis avec l’attribut `aria-label`. La valeur de `aria-label`’attribut est renseignée à partir de la valeur du symbole de localisation du bouton. Lorsqu’un bouton est désactivé, `aria-disabled` attribut est défini en conséquence.

La vue principale comporte des `application` de rôle. Une brève description de la vue principale est fournie en `aria-roledescription`, avec la valeur définie par le symbole de localisation `ROLE_DESCRIPTION` du composant de vue principale correspondant. Les conseils de navigation pour les utilisateurs d’un clavier sont fournis à l’aide de `aria-describedby`. Le texte du conseil d’utilisation provient du symbole de localisation `USAGE_HINT`. Si un libellé est défini dans le champ UserData d’une ressource, l’attribut `aria-label` est défini avec la valeur de ce libellé.

Les composants qui affichent des échantillons ont le rôle `listbox` avec `aria-label` attribut défini sur la valeur du symbole de localisation `LABEL` de ce composant. Les échantillons individuels ont le rôle `option` avec les attributs `aria-setsize` et `aria-posinset` pour décrire la position de l’échantillon dans l’ensemble. Si une nuance est sélectionnée, elle reçoit l’attribut `aria-selected` défini sur `true`.

