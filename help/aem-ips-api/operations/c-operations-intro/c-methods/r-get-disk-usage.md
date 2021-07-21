---
description: Renvoie des informations sur la structure d’une société (nombre de fichiers, etc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 13%

---

# getDiskUsage{#getdiskusage}

Renvoie des informations sur la structure d’une société (nombre de fichiers, etc.).

## Types d’utilisateurs autorisés {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Entrée (getDiskUsageParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Le gestionnaire à la société dont vous souhaitez obtenir l’utilisation du disque. |

**Sortie (getDiskUsageReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | Oui | Tableau de l’utilisation du disque de l’entreprise. |

## Exemples {#section-cb16a97badc94076ad5da277db5ed16a}

Le nom de cette demande est trompeur. Plutôt que de renvoyer uniquement une valeur scalaire qui reflète la quantité d’espace disque qu’une entreprise utilise, elle obtient d’autres informations sur la structure d’une entreprise également.

**Request**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**Réponse**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```
