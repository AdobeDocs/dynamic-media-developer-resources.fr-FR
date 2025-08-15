---
description: Créez une nouvelle zone cliquable ou modifiez une carte existante.
solution: Experience Manager
title: Enregistrer la zone cliquable
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 8%

---

# Enregistrer la zone cliquable{#saveimagemap}

Créez une nouvelle zone cliquable ou modifiez une carte existante.

Syntaxe

## Types d’utilisateurs autorisés {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à l’actif.

## Paramètres {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Entrée (saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Obligatoire </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> CompanyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée de la société avec la zone cliquable que vous souhaitez enregistrer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> AssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée de la ressource d’image à laquelle la zone cliquable appartient. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Poignée de carte d’image </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Poignée de la zone cliquable. Crée une zone cliquable si elle est nulle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> nom </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom de la zone cliquable créée ou enregistrée. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Type </span> de forme </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Choix de la forme de la région. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> région </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Liste de points délimités par des virgules qui définissent la région. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> action </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Valeur <span class="codeph"> href </span> associée à la zone cliquable, comme spécifié dans l’interface IPS. </p> <p>Pour obtenir la <span class="codeph"> valeur href </span> , cliquez sur l’image dans l’interface IPS, copiez et collez l’URL dans cet élément, puis formatez l’URL IPS en tant qu’URL appropriée. Par exemple, <span class="codeph"> &amp; </span> devient <span class="codeph"> &amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> position </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Ordre dans la liste des zones cliquables (axe Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Activé </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée de carte d’image | `xsd:string` | Oui | Poignée de la zone cliquable nouvelle ou modifiée. |

## Exemples {#section-fdac488b640f427c8aa3d549c5032851}

Cet exemple de code crée une nouvelle zone cliquable pour un actif. Il utilise un type de forme déterminé par une constante de chaîne de forme de région et renvoie une poignée à la nouvelle zone cliquable.

**Demander**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**Réponse**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
