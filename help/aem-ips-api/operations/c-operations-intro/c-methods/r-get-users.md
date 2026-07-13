---
description: Obtient un tableau d'utilisateurs tel que spécifié par les descripteurs de rôle d'entreprise, de groupe et d'utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
TQID: 'https://experienceleague.adobe.com/17FQLNVfRg84FeVetVfuTWoLRMf8ugBwXBi2CpmLZfI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 9%

---

# getUsers{#getusers}

Obtient un tableau d&#39;utilisateurs tel que spécifié par les descripteurs de rôle d&#39;entreprise, de groupe et d&#39;utilisateur. Cette opération vous permet de trier les utilisateurs renvoyés et de filtrer par caractère.

## Types d’utilisateurs autorisés {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| includeInactive | `xsd:boolean` | Non | Incluez ou excluez les utilisateurs inactifs. Les utilisateurs administrateurs non-IPS doivent être membres actifs d&#39;au moins une société pour être autorisés à effectuer des appels API. Une erreur d’autorisation est renvoyée si l’utilisateur n’a pas d’adhésions d’entreprise actives. |
| includeInvalid | `xsd:boolean` | Non | Permet d’inclure ou d’exclure des utilisateurs non valides. |
| companyHandleArray | `types:HandleArray` | Non | Filtrez les résultats par entreprise. |
| groupHandleArray | `types:HandleArray` | Non | Filtrez les résultats par groupe. |
| userRoleArray | `types:StringArray` | Non | Filtrez les résultats par rôle d’utilisateur. |
| charFilterField | `xsd:string` | Non | Filtrer les résultats en fonction du préfixe de chaîne du champ (voir [!DNL Trash State).] |
| charFilter | `xsd:string` | Non | Filtrez les résultats selon un caractère spécifique. |
| sortBy | `xsd:string` | Non | Choix des champs de tri des utilisateurs. |
| recordsPerPage | `xsd:int` | Non | Retourne le nombre spécifié d&#39;enregistrements par page. |
| resultsPage | `xsd:int` | Non | Page de résultats. |

**Output (getUsersReturn)**

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

