---
description: Un utilisateur de ressources et de types dans le système.
solution: Experience Manager
title: Utilisateur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# [!DNL User]{#user}

Un utilisateur de ressources et de types dans le système.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| userHandle | `xsd:string` | Identifiant utilisateur. |
| firstName | `xsd:string` | Prénom de l’utilisateur. |
| lastName | `xsd:string` | Nom de l’utilisateur. |
| e-mail | `xsd:string` | adresse électronique. |
| defaultRole | `xsd:string` | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Cependant, le rôle de l’utilisateur `IpsAmin` remplace les autres rôles utilisateur. |
| isValid | `xsd:boolean` | Détermine si l’utilisateur est valide. |
| passwordExpires | `xsd:dateTime` | Définit la date d’expiration du mot de passe. |
