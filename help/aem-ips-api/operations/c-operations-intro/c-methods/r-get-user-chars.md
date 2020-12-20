---
description: Obtient une liste des caractères utilisés dans un champ particulier.
seo-description: Obtient une liste des caractères utilisés dans un champ particulier.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# getUserChars{#getuserchars}

Obtient une liste des caractères utilisés dans un champ particulier.

Syntaxe

## Types d’utilisateur autorisés {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Entrée (getUserCharsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`charField`*` | `xsd:string` | Oui | Détermine l’état de la corbeille à rechercher. |
| ` *`includeInactive`*` | `xsd:boolean` | Oui | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs administrateurs non-IPS doivent être membres principaux d&#39;au moins une société pour être autorisés à effectuer des appels d&#39;API. Une erreur d&#39;autorisation est renvoyée si l&#39;utilisateur n&#39;a pas d&#39;abonnement à une société principale. |
| ` *`includInvalid`*` | `xsd:boolean` | Non | Incluez ou excluez des utilisateurs non valides. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats en fonction de la société. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Non | Filtres des résultats en fonction des groupes. |
| ` *`userRoleArray`*` | `types:StringArray` | Non | Filtres des résultats en fonction du rôle utilisateur. |
| ` *`numChars`*` | `xsd:int` | Non | Activez >1 caractère. |

**Output (getUserCharsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userCharsArray`*` | `types:StringArray` | Oui | Tableau de préfixes de caractères. |

## Exemples {#section-3702f165e8b041139a6144f4a76ca25f}

Cet exemple de code renvoie :

* Premiers caractères des noms des utilisateurs d’une société spécifique.
* Ensemble de groupes.
* Ensemble de rôles utilisateur.

La constante de chaîne Champs de filtre de caractères utilisateur détermine le type de caractères d’utilisateur renvoyés.

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

