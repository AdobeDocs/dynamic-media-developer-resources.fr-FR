---
description: Utilisateur de ressources et de types dans le système.
seo-description: Utilisateur de ressources et de types dans le système.
seo-title: Utilisateur
solution: Experience Manager
title: Utilisateur
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Utilisateur{#user}

Utilisateur de ressources et de types dans le système.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Identifiant utilisateur. |
| ` *`firstName`*` | `xsd:string` | Prénom de l’utilisateur. |
| ` *`lastName`*` | `xsd:string` | Nom d’utilisateur. |
| ` *`e-mail`*` | `xsd:string` | adresse électronique. |
| ` *`defaultRole`*` | `xsd:string` | Définit le rôle d’un utilisateur dans chaque auquel il appartient. Cependant, le rôle utilisateur `IpsAmin` remplace les autres rôles utilisateur. |
| ` *`isValid`*` | `xsd:boolean` | Détermine si l’utilisateur est valide. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Définit la date d’expiration du mot de passe. |

