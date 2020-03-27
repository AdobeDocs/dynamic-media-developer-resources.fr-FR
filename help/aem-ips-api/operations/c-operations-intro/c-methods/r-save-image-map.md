---
description: Créez une zone cliquable ou modifiez une zone cliquable existante.
seo-description: Créez une zone cliquable ou modifiez une zone cliquable existante.
seo-title: saveImageMap
solution: Experience Manager
title: saveImageMap
topic: Scene7 Image Production System API
uuid: 9714fc99-2259-4766-96d7-fe2f9fd2f341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageMap{#saveimagemap}

Créez une zone cliquable ou modifiez une zone cliquable existante.

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
>L’utilisateur doit disposer d’un accès en lecture et en écriture au fichier.

## Paramètres {#section-64f7f5fd8f954fba9fa30eeee556863a}

**Input (saveImageMapParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée vers le avec la zone cliquable à enregistrer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fichierHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée du fichier d’image auquel appartient la zone cliquable. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Poignée de la zone cliquable. Crée une zone cliquable si NULL. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom de la zone cliquable créée ou enregistrée. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> shapeType </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Forme de choix de région. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> région </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> de points délimités par des virgules qui définissent la région. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> action </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> <p>Valeur <span class="codeph"> href </span> associée à la zone cliquable, spécifiée dans l'interface IPS. </p> <p>Pour obtenir la <span class="codeph"> valeur href </span> , cliquez sur l'image dans l'interface IPS, copiez et collez l'URL dans cet élément, puis formatez l'URL IPS en tant qu'URL appropriée. Par exemple, <span class="codeph"> &amp; </span> devient <span class="codeph"> &amp;amp; </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> position </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Ordre dans le  des zones cliquables (axe Z). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> activé </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**Output (saveImageMapReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Oui | Identifiant de la zone cliquable nouvelle ou modifiée. |

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

