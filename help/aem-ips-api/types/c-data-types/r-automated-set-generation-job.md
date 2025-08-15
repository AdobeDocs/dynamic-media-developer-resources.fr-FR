---
description: Regroupez les fichiers en jeux à l’aide d’un tableau de liste de gestion des ressources.
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 4%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

Regroupez les fichiers en jeux à l’aide d’un tableau de liste de gestion des ressources.

Syntaxe

## Paramètres {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3">Tableau de descripteurs de ressources utilisé pour créer l’ensemble. <p>Par défaut, 1 000 est le nombre maximal de ressources que vous pouvez avoir dans le tableau. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Chemin d’accès au dossier dans lequel vous souhaitez enregistrer les jeux. Enregistre dans le dossier racine d’entreprise par défaut. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Définit un indicateur pour indiquer si les ressources doivent être publiées ou non. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> de sous-domaines:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Tableau de scripts de génération définis que vous pouvez exécuter sur les fichiers chargés. Voir <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Configurez une notification électronique automatisée pour le traitement. </p> </td> 
  </tr> 
 </tbody> 
</table>

**options emailSetting**

Le paramètre `emailSetting` comprend les options suivantes :

| Option | Renvoie |
|---|---|
| `All` | Toutes les notifications de traitement (erreurs, avertissements, fin) au destinataire spécifié. |
| `Error` | Erreurs de traitement du destinataire spécifié. |
| `ErrorAndWarning` | Erreurs et avertissements de traitement du destinataire spécifié. |
| `JobCompletion` | Notification de fin de tâche au destinataire spécifié. |
| `None` | Le traitement n’envoie aucune notification de traitement au destinataire spécifié. |

## Exemple {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```
