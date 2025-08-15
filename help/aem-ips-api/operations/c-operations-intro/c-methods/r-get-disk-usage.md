---
description: Renvoie des informations sur la structure d’une société (nombre de fichiers, etc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 11%

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
| CompanyHandle | `xsd:string` | Oui | Poignée de l’entreprise dont vous souhaitez obtenir l’utilisation du disque. |

**Output (getDiskUsageReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau de disques d’utilisation | `types:DiskUsageArray` | Oui | Tableau d’utilisation du disque de l’entreprise. |

## Exemples {#section-cb16a97badc94076ad5da277db5ed16a}

Le nom de cette demande est trompeur. Plutôt que de renvoyer simplement une valeur scalaire qui reflète la quantité d’espace disque utilisée par une entreprise, elle obtient également d’autres informations sur la structure d’une entreprise.

**Demander**

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
