---
description: Obtient une liste des caractères utilisés dans un champ particulier.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 11%

---

# getUserChars{#getuserchars}

Obtient une liste des caractères utilisés dans un champ particulier.

Syntaxe

## Types d’utilisateurs autorisés {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Entrée (getUserCharsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | Oui | Détermine l’état de la corbeille à rechercher. |
| `*`includeInactive`*` | `xsd:boolean` | Oui | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs non administrateurs d’IPS doivent être un membre principal d’au moins une société pour être autorisés à effectuer des appels d’API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a pas d’appartenances principales à la société. |
| `*`includeInvalid`*` | `xsd:boolean` | Non | Incluez ou excluez des utilisateurs non valides. |
| `*`companyHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats en fonction de l’entreprise. |
| `*`groupHandleArray`*` | `types:HandleArray` | Non | Filtre les résultats en fonction des groupes. |
| `*`userRoleArray`*` | `types:StringArray` | Non | Filtre les résultats en fonction du rôle de l’utilisateur. |
| `*`numChars`*` | `xsd:int` | Non | Activer >1 caractère. |

**Sortie (getUserCharsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | Oui | Tableau de préfixes de caractères. |

## Exemples {#section-3702f165e8b041139a6144f4a76ca25f}

Cet exemple de code renvoie :

* Premiers caractères des noms des utilisateurs d’une société spécifique.
* Ensemble de groupes.
* Ensemble de rôles utilisateur.

La constante de chaîne Champs de filtre de caractères de l’utilisateur détermine le type de caractères d’utilisateur renvoyés.

**Request**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Réponse**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
