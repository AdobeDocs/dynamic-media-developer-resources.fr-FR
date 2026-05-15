---
description: Crée une vue prédéfinie qui détermine ce qu’un utilisateur peut voir. La visionneuse peut être de n’importe quel type disponible dans IPS. La vue prédéfinie est appliquée lors de la publication des ressources.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
TQID: 'https://experienceleague.adobe.com/0RlldrqgWyv0YeP-QqtiVqlDpWtGk60mOWf-w9ageYA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

Crée une vue prédéfinie qui détermine ce qu’un utilisateur peut voir. La visionneuse peut être de n’importe quel type disponible dans IPS. La vue prédéfinie est appliquée lors de la publication des ressources.

Syntaxe

## Types d’utilisateurs autorisés {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Input (createViewerPresetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Descripteur de la société qui contient les paramètres prédéfinis de visionneuse et les ressources. |
| folderHandle | `xsd:string` | Oui | L’identificateur du dossier contenant les ressources. |
| nom | `xsd:string` | Oui | Nom de la visionneuse. |
| type | `xsd:string` | Oui | Type de visionneuse. |
| configSettingArray | `types:ConfigSettingArray` | Non | Tableau contenant les noms, les valeurs et les descripteurs des images auxquelles vous appliquez des paramètres prédéfinis. |

**Output (createViewerPresetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | Oui | Gestionnaire du paramètre prédéfini pour la visionneuse. |

## Exemples {#section-c88ea63536f3461cbe4677ba53f875dd}

Cet exemple de code crée un paramètre prédéfini de lecteur vidéo. La réponse renvoie une poignée au paramètre prédéfini.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Réponse**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
