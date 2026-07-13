---
description: Renvoie un tableau de toutes les sociétés.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
TQID: 'https://experienceleague.adobe.com/B2wkv6Xvuvg17yqUucjIx170K4YmznQgBrJiVgLe2qg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 18%

---

# getAllCompanies{#getallcompanies}

Renvoie un tableau de toutes les sociétés.

Syntaxe

## Types d’utilisateurs autorisés {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Paramètres {#section-efd74992e6904ebabe7383b577af4fdb}

**Input (getAllCompaniesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| includeExpired | `xsd:boolean` | Oui | Définissez cette variable sur true pour renvoyer les sociétés expirées et non expirées. |

**Output (getAllCompaniesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyArray | `types:CompanyArray` | Oui | Tableau d’entreprises. |

## Exemples {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Cet exemple de code renvoie toutes les sociétés dans IPS d’un tableau. Notez que l’exemple de réponse est tronqué par souci de concision.

**Requête**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**Réponse**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```

