---
description: Met à jour les valeurs du dictionnaire de balises pour un champ de balise.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
TQID: 'https://experienceleague.adobe.com/ELmOHY1OW3c3AteQOjludnMS4jRLcJX9KezAhFkQj-Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 12%

---

# updateTagFieldValues{#updatetagfieldvalues}

Met à jour les valeurs du dictionnaire de balises pour un champ de balise.

Syntaxe

## Types d’utilisateurs autorisés {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-0a3a4bab026746238c9d4009caf42e94}

**Input (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant de la société. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant du champ de balise. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types : TagValueUpdateArray</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4">Tableau des valeurs de champ de balise à mettre à jour. <p>Remarque : met à jour uniquement les valeurs de chaîne de balise. N’affecte pas les associations de ressources. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateTagFieldValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de champs de balise mis à jour avec succès. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de mettre à jour les champs de balise. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de mettre à jour les champs de balise. |
| warningDetailArray | `types:TagValueUpdateFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté de mettre à jour les champs de balise. |
| errorDetailArray | `types:TagValueUpdateFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté de mettre à jour les champs de balise. |

## Exemples {#section-bb4dcf97044c4675974c9b8d27674001}

**Requête**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Réponse**

```java {.line-numbers}
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

