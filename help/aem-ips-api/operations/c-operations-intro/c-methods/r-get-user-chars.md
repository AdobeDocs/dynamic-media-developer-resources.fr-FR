---
description: Obtient un  des caractères utilisés dans un champ particulier.
seo-description: Obtient un  des caractères utilisés dans un champ particulier.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUserChars{#getuserchars}

Obtient un  des caractères utilisés dans un champ particulier.

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
| ` *`charField`*` | `xsd:string` | Oui | Détermine l’état de la corbeille à rechercher. |
| ` *`includeInactive`*` | `xsd:boolean` | Oui | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs non administrateurs d&#39;IPS doivent être membres actifs d&#39;au moins un  pour être autorisés à effectuer des appels d&#39;API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a pas d’abonnement  actif. |
| ` *`includInvalid`*` | `xsd:boolean` | Non | Incluez ou excluez des utilisateurs non valides. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats en fonction des  du. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Non |  résultats basés sur des groupes. |
| ` *`userRoleArray`*` | `types:StringArray` | Non | Résultats  en fonction du rôle utilisateur. |
| ` *`numChars`*` | `xsd:int` | Non | Activez >1 caractère. |

**Output (getUserCharsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userCharsArray`*` | `types:StringArray` | Oui | Tableau de préfixes de caractères. |

## Exemples {#section-3702f165e8b041139a6144f4a76ca25f}

Cet exemple de code renvoie :

* Premiers caractères des noms des utilisateurs d’un  spécifique.
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

