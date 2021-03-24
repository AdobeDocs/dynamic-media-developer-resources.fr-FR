---
description: Utilisateur des ressources et types du système.
solution: Experience Manager
title: Utilisateur
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---


# Utilisateur{#user}

Utilisateur des ressources et types du système.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | Identifiant utilisateur. |
| `*`firstName`*` | `xsd:string` | Prénom de l’utilisateur. |
| `*`lastName`*` | `xsd:string` | Nom d’utilisateur. |
| `*`e-mail`*` | `xsd:string` | adresse électronique. |
| `*`defaultRole`*` | `xsd:string` | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Cependant, le rôle utilisateur `IpsAmin` remplace les autres rôles utilisateur. |
| `*`isValid`*` | `xsd:boolean` | Détermine si l’utilisateur est valide. |
| `*`passwordExpires`*` | `xsd:dateTime` | Définit la date d’expiration du mot de passe. |

