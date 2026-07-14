---
description: Obtient une liste des caractères utilisés dans un champ particulier.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
TQID: 'https://experienceleague.adobe.com/ojFrVXletWbKwGTjfJIfRI9M9BBJT7zj4AGrvVMP6T8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 10%

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

**Input (getUserCharsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| charField | `xsd:string` | Oui | Détermine l’état de la corbeille à rechercher. |
| includeInactive | `xsd:boolean` | Oui | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs administrateurs non-IPS doivent être membres actifs d&#39;au moins une société pour être autorisés à effectuer des appels API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a pas d’adhésions d’entreprise actives. |
| includeInvalid | `xsd:boolean` | Non | Incluez ou excluez les utilisateurs non valides. |
| companyHandleArray | `types:HandleArray` | Non | Filtrez les résultats en fonction de la société. |
| groupHandleArray | `types:HandleArray` | Non | Filtre les résultats en fonction des groupes. |
| userRoleArray | `types:StringArray` | Non | Filtre les résultats en fonction du rôle de l’utilisateur. |
| numChars | `xsd:int` | Non | Activez >1 caractère. |

**Output (getUserCharsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Oui | Tableau de préfixes de caractères. |

## Exemples {#section-3702f165e8b041139a6144f4a76ca25f}

Cet exemple de code renvoie :

* Prénoms des noms des utilisateurs d&#39;une société spécifique.
* Ensemble de groupes.
* Ensemble de rôles utilisateur.

La constante de chaîne Champs de filtre de graphique utilisateur détermine le type de caractères utilisateur renvoyé.

**Requête**

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

