---
description: Obtient un tableau d'utilisateurs tel que spécifié par les poignées de société, de groupe et de rôle utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 10%

---


# getUsers{#getusers}

Obtient un tableau d&#39;utilisateurs tel que spécifié par les poignées de société, de groupe et de rôle utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.

## Types d’utilisateur autorisés {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | Non | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs administrateurs non-IPS doivent être membres principaux d&#39;au moins une société pour être autorisés à effectuer des appels d&#39;API. Une erreur d&#39;autorisation est renvoyée si l&#39;utilisateur n&#39;a pas d&#39;abonnement à une société principale. |
| `*`includeInvalid`*` | `xsd:boolean` | Non | Vous permet d’inclure/d’exclure des utilisateurs non valides. |
| `*`companyHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats par société. |
| `*`groupHandleArray`*` | `types:HandleArray` | Non | Filtrez les résultats par groupe. |
| `*`userRoleArray`*` | `types:StringArray` | Non | Filtrez les résultats par rôle utilisateur. |
| `*`charFilterField`*` | `xsd:string` | Non | Filtrer les résultats par préfixe de chaîne de champ (voir [!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | Non | Filtrez les résultats selon un caractère spécifique. |
| `*`sortBy`*` | `xsd:string` | Non | Choix des champs de tri des utilisateurs. |
| `*`recordsPerPage`*` | `xsd:int` | Non | Renvoie le nombre spécifié d’enregistrements par page. |
| `*`resultsPage`*` | `xsd:int` | Non | Page de résultats. |

**Sortie (getUsersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Oui | Tableau d’utilisateurs. |

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

