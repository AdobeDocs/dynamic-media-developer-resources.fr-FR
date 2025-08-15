---
description: Obtient la liste des caractères utilisés dans un champ particulier.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

---

# getUserChars{#getuserchars}

Obtient la liste des caractères utilisés dans un champ particulier.

Syntaxe

## Types d’utilisateurs autorisés {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Input (getUserCharsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Champ de caractères | `xsd:string` | Oui | Détermine l’état de la corbeille à rechercher. |
| includeInactive | `xsd:boolean` | Oui | Inclure ou exclure des utilisateurs inactifs. Les utilisateurs administrateurs non-IPS doivent être un membre actif d’au moins une entreprise pour être autorisés à effectuer des appels d’API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a aucun abonnement d’entreprise actif. |
| includInvalid | `xsd:boolean` | Non | Inclure ou exclure des utilisateurs non valides. |
| companyHandleArray | `types:HandleArray` | Non | Filtrage des résultats en fonction de l’entreprise. |
| GroupHandleArray | `types:HandleArray` | Non | Filtre les résultats en fonction des groupes. |
| UserRoleArray | `types:StringArray` | Non | Filtre les résultats en fonction du rôle utilisateur. |
| numChars | `xsd:int` | Non | Activez >1 caractère. |

**Output (getUserCharsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Oui | Tableau de préfixes de caractères. |

## Exemples {#section-3702f165e8b041139a6144f4a76ca25f}

Cet exemple de code renvoie :

* Premiers caractères des noms de famille des utilisateurs d’une entreprise spécifique.
* Ensemble de groupes.
* Ensemble de rôles utilisateur.

La constante de chaîne User Char Filter Fields détermine le type de caractères renvoyés.

**Demander**

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
