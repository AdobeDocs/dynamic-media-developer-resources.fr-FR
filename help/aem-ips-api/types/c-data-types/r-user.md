---
description: Utilisateur des ressources et des types dans le système.
solution: Experience Manager
title: Utilisateur
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 9%

---

# [!DNL User]{#user}

Utilisateur des ressources et des types dans le système.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| userHandle | `xsd:string` | Handle utilisateur. |
| firstName | `xsd:string` | Prénom de l’utilisateur. |
| lastName | `xsd:string` | Nom de l’utilisateur. |
| e-mail | `xsd:string` | adresse électronique. |
| defaultRole | `xsd:string` | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Cependant, le rôle d’utilisateur remplace `IpsAmin` d’autres rôles d’utilisateur. |
| isValid | `xsd:boolean` | Détermine si l’utilisateur est valide. |
| passwordExpires | `xsd:dateTime` | Définit la date d’expiration du mot de passe. |
