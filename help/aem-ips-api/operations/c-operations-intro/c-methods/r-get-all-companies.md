---
description: Renvoie un tableau de toutes les sociétés.
seo-description: Renvoie un tableau de toutes les sociétés.
seo-title: getAllCompanies
solution: Experience Manager
title: getAllCompanies
uuid: bc2d82b1-e020-4dfe-9704-601ef5aa2111
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 17%

---


# getAllCompanies{#getallcompanies}

Renvoie un tableau de toutes les sociétés.

Syntaxe

## Types d’utilisateur autorisés {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Paramètres {#section-efd74992e6904ebabe7383b577af4fdb}

**Entrée (getAllCompaniesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | Oui | Définissez cette variable sur true pour renvoyer les sociétés expirées et non expirées. |

**Output (getAllCompaniesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | Oui | Tableau de sociétés. |

## Exemples {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Cet exemple de code renvoie toutes les sociétés d&#39;IPS dans un tableau. Notez que l’exemple de réponse est tronqué pour plus de concision.

**Request**

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

