---
description: Créez une zone cliquable ou modifiez une zone cliquable existante.
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 15%

---


# saveImageMap{#saveimagemap}

Créez une zone cliquable ou modifiez une zone cliquable existante.

Syntaxe

## Types d’utilisateur autorisés {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée vers la société avec la zone cliquable à enregistrer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée du fichier d’image auquel appartient la zone cliquable. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Poignée de la zone cliquable. Crée une zone cliquable si NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom de la zone cliquable créée ou enregistrée. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Choix de la forme de la région. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> region  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Liste de points délimités par des virgules qui définissent la région. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> action  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Valeur <span class="codeph"> href </span> associée à la zone cliquable, comme indiqué dans l'interface IPS. </p> <p>Pour obtenir la valeur <span class="codeph"> href </span>, cliquez sur l'image dans l'interface IPS, copiez et collez l'URL dans cet élément, puis formatez l'URL IPS en tant qu'URL appropriée. Par exemple, <span class="codeph"> &amp; </span> devient <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Ordre dans la liste des zones cliquables (axe Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> enabled  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Oui | Poignée de la nouvelle zone cliquable ou de la zone cliquable modifiée. |

## Exemples {#section-fdac488b640f427c8aa3d549c5032851}

Cet exemple de code crée une nouvelle zone cliquable pour un fichier. Il utilise un type de forme déterminé par une constante de chaîne de forme de région et renvoie une poignée à la nouvelle zone cliquable.

**Request**

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

