---
description: Récupère un tableau d’utilisateurs tel que spécifié par les  de, les groupes et les gestionnaires de rôle utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.
seo-description: Récupère un tableau d’utilisateurs tel que spécifié par les  de, les groupes et les gestionnaires de rôle utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Scene7 Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUsers{#getusers}

Récupère un tableau d’utilisateurs tel que spécifié par les  de, les groupes et les gestionnaires de rôle utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.

## Types d’utilisateurs autorisés {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`includeInactive`*` | `xsd:boolean` | Non | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs non administrateurs d&#39;IPS doivent être membres actifs d&#39;au moins un  pour être autorisés à effectuer des appels d&#39;API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a pas d’abonnement  actif. |
| ` *`includeInvalid`*` | `xsd:boolean` | Non | Vous permet d’inclure/d’exclure des utilisateurs non valides. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats par . |
| ` *`groupHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats par groupe. |
| ` *`userRoleArray`*` | `types:StringArray` | Non | Filtrez les résultats par rôle utilisateur. |
| ` *`charFilterField`*` | `xsd:string` | Non | Filtrage des résultats par préfixe de chaîne du champ (voir [!DNL Trash State).] |
| ` *`charFilter`*` | `xsd:string` | Non | Filtrez les résultats selon un caractère spécifique. |
| ` *`sortBy`*` | `xsd:string` | Non | Choix des champs de tri des utilisateurs. |
| ` *`recordsPerPage`*` | `xsd:int` | Non | Renvoie le nombre spécifié d’enregistrements par page. |
| ` *`resultsPage`*` | `xsd:int` | Non | Page de résultats. |

**Output (getUsersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userArray`*` | `types:UserArray` | Oui | Tableau d’utilisateurs. |

## Exemples {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Cet exemple de code renvoie le tableau des utilisateurs pour plusieurs paramètres facultatifs. Les rôles utilisateur, les champs de filtre de caractères utilisateur et les champs de tri utilisateur sont déterminés à l’aide de constantes de chaîne spécifiques.

**Request**

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

