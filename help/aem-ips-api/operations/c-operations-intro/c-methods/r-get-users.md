---
description: Obtient un tableau d’utilisateurs tel que spécifié par les gestionnaires de rôles d’entreprise, de groupe et d’utilisateur. Cette opération permet de trier les utilisateurs renvoyés et les filtrer par caractère.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 9%

---

# getUsers{#getusers}

Obtient un tableau d’utilisateurs tel que spécifié par les gestionnaires de rôles d’entreprise, de groupe et d’utilisateur. Cette opération permet de trier les utilisateurs renvoyés et les filtrer par caractère.

## Types d’utilisateurs autorisés {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| includeInactive | `xsd:boolean` | Non | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs non administrateurs d’IPS doivent être membres actifs d’au moins une société pour être autorisés à effectuer des appels d’API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a aucun abonnement actif à la société. |
| includeInvalid | `xsd:boolean` | Non | Vous permet d’inclure/d’exclure des utilisateurs non valides. |
| companyHandleArray | `types:HandleArray` | Non | Filtrez les résultats par société. |
| groupHandleArray | `types:HandleArray` | Non | Filtrage des résultats par groupe. |
| userRoleArray | `types:StringArray` | Non | Filtrage des résultats par rôle utilisateur. |
| charFilterField | `xsd:string` | Non | Filtrage des résultats par préfixe de chaîne du champ (voir [!DNL Trash State).] |
| charFilter | `xsd:string` | Non | Filtrez les résultats selon un caractère spécifique. |
| sortBy | `xsd:string` | Non | Choix des champs de tri des utilisateurs. |
| recordsPerPage | `xsd:int` | Non | Renvoie le nombre d’enregistrements spécifié par page. |
| resultsPage | `xsd:int` | Non | Page Résultats . |

**Sortie (getUsersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userArray | `types:UserArray` | Oui | Tableau d’utilisateurs. |

## Exemples {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Cet exemple de code renvoie le tableau des utilisateurs pour plusieurs paramètres facultatifs. Les rôles utilisateur, les champs de filtre de caractères utilisateur et les champs de tri utilisateur sont déterminés à l’aide de constantes de chaîne spécifiques.

**Requête**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Réponse**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
