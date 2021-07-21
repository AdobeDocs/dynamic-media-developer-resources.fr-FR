---
description: Renvoie toutes les valeurs d’un champ de métadonnées.
solution: Experience Manager
title: getDistinctMetadataValues
feature: Dynamic Media Classic,SDK/API,Métadonnées
role: Developer,Admin
exl-id: 1987d8b0-64e4-49be-af45-98e4c6542e5f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 22%

---

# getDistinctMetadataValues{#getdistinctmetadatavalues}

Renvoie toutes les valeurs d’un champ de métadonnées.

Syntaxe

## Types d’utilisateurs autorisés {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-600f36a32ff147cb83149943d37843e2}

**Entrée (getDistinctMetadataValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société pour laquelle vous souhaitez obtenir des données. |
| `*`metadataKey`*` | `xsd:string` | Oui | Clé de métadonnées en notation par points. |

**Sortie (getDistinctMetadataValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`valueArray`*` | `types:ValueArray` | Oui | Valeurs du champ de métadonnées demandé. |

## Exemples {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**Request**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Réponse**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```
