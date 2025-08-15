---
description: Crée une vue prédéfinie qui détermine ce que l’utilisateur peut voir. La visionneuse peut être de n’importe quel type disponible dans IPS. La vue prédéfinie est appliquée lors de la publication des ressources.
solution: Experience Manager
title: Créer un paramètre prédéfini de visionneuse
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 12%

---

# Créer un paramètre prédéfini de visionneuse{#createviewerpreset}

Crée une vue prédéfinie qui détermine ce que l’utilisateur peut voir. La visionneuse peut être de n’importe quel type disponible dans IPS. La vue prédéfinie est appliquée lors de la publication des ressources.

Syntaxe

## Types d’utilisateurs autorisés {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Entrée (createViewerPresetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Pseudo de l’entreprise qui contient les paramètres prédéfinis et les ressources de visionneuse. |
| poignée de dossier | `xsd:string` | Oui | Handle du dossier qui contient les ressources. |
| nom | `xsd:string` | Oui | Nom de la visionneuse. |
| type | `xsd:string` | Oui | Type de visionneuse. |
| Paramètre de configuration | `types:ConfigSettingArray` | Non | Tableau contenant les noms, les valeurs et les descripteurs des images auxquelles vous appliquez des paramètres prédéfinis. |

**Output (createViewerPresetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée préréglée de visionneuse | `xsd:string` | Oui | Poignée du paramètre prédéfini à la visionneuse. |

## Exemples {#section-c88ea63536f3461cbe4677ba53f875dd}

Cet échantillon de code crée un paramètre prédéfini de lecteur vidéo. La réponse renvoie une poignée au paramètre prédéfini.

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
