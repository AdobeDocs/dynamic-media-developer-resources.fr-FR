---
description: Obtient un tableau d’utilisateurs tel que spécifié par les descripteurs de rôle de société, de groupe et d’utilisateur. Cette opération permet de trier les utilisateurs récurrents et de filtrer les données par caractère.
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

Obtient un tableau d’utilisateurs tel que spécifié par les descripteurs de rôle de société, de groupe et d’utilisateur. Cette opération permet de trier les utilisateurs récurrents et de filtrer les données par caractère.

## Types d’utilisateurs autorisés {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| includeInactive | `xsd:boolean` | Non | Inclure ou exclure des utilisateurs inactifs. Les utilisateurs administrateurs non-IPS doivent être un membre actif d’au moins une entreprise pour être autorisés à effectuer des appels d’API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a aucun abonnement d’entreprise actif. |
| includeInvalid | `xsd:boolean` | Non | Vous permet d’inclure/d’exclure des utilisateurs non valides. |
| companyHandleArray | `types:HandleArray` | Non | Filtrer les résultats par société. |
| GroupHandleArray | `types:HandleArray` | Non | Filtrer les résultats par groupe. |
| UserRoleArray | `types:StringArray` | Non | Filtrer les résultats par rôle utilisateur. |
| CharFilterField | `xsd:string` | Non | Filtrer les résultats selon le préfixe de chaîne du champ (voir [!DNL Trash State).] |
| Filtre de caractères | `xsd:string` | Non | Filtrer les résultats selon un caractère spécifique. |
| Tri par | `xsd:string` | Non | Choix des champs de tri des utilisateurs. |
| recordsPerPage | `xsd:int` | Non | Renvoie le nombre spécifié d’enregistrements par page. |
| Page de résultats | `xsd:int` | Non | Page Résultats. |

**Output (getUsersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau d’utilisateurs | `types:UserArray` | Oui | Un éventail d’utilisateurs. |

## Exemples {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Cet exemple de code renvoie le tableau des utilisateurs pour plusieurs paramètres facultatifs. Les rôles utilisateur, les champs de filtre de caractères utilisateur et les champs de tri utilisateur sont déterminés à l’aide de constantes de chaîne spécifiques.

**Demander**

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
