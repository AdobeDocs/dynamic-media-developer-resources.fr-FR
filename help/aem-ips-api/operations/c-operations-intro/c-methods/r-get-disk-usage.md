---
description: Renvoie des informations sur la structure d’une société (nombre de fichiers, etc.).
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 13%

---


# getDiskUsage{#getdiskusage}

Renvoie des informations sur la structure d’une société (nombre de fichiers, etc.).

## Types d’utilisateur autorisés {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**Entrée (getDiskUsageParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société dont vous souhaitez obtenir l&#39;utilisation du disque. |

**Output (getDiskUsageReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | Oui | Tableau de l&#39;utilisation des disques de société. |

## Exemples {#section-cb16a97badc94076ad5da277db5ed16a}

Le nom de cette demande est trompeur. Plutôt que de renvoyer uniquement une valeur scalaire qui reflète l&#39;espace disque utilisé par une société, elle obtient d&#39;autres informations sur la structure d&#39;une société également.

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

