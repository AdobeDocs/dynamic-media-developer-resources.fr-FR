---
description: Obtient les actifs associés à un actif spécifié et les détails de leur relation.
seo-description: Obtient les actifs associés à un actif spécifié et les détails de leur relation.
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

Obtient les actifs associés à un actif spécifié et les détails de leur relation.

Syntaxe

## Types d’utilisateurs autorisés {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Entrée (getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sociétéHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Traitement du  propriétaire de la ressource. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée de ressource. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau des champs de réponse souhaités. Voir response-FieldArray/excludeFieldArray dans l’introduction. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau des champs de réponse exclus. Voir response-FieldArray/excludeFieldArray dans l’introduction. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AssetArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de ressources de jeu et de modèle contenant la ressource de champ spécifique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> MemberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AssetArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de ressources contenues dans le jeu ou le modèle de ressources spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AssetArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de ressources référencées dans une URL de calque ou de modèle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:AssetArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau de ressources qui possèdent la ressource spécifiée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> tableau <span class="varname"></span> dérivé </span> </td> 
   <td colname="col2"> <span class="codeph"> type:AssetArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Tableau des ressources utilisées pour générer la ressource spécifiée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Le <span class="codeph"> générateurArray</span>  la manière dont cet actif a été créé. Par exemple, si <span class="codeph"> assetHandler</span> était une page d’image d’un fichier PDF, cela contiendrait l’outil de processeur PDF et référencerait le fichier PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Le <span class="codeph"> tableau</span> généré inverse la manière dont ce fichier a été créé. Par exemple, le <span class="codeph"> tableau</span> généré peut contenir le  des images générées à partir de ce <span class="codeph"> gestionnaire</span> de ressources s’il s’agit d’un fichier PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:Asset</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Informations sur l’actif de miniature associées à l’actif de requête. Si aucune ressource miniature n’est affectée, le champ est omis dans la réponse. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez utiliser les paramètres `responseFieldArray` ou `excludeFieldArray` limiter la taille de la réponse. En particulier, les `GenerationInfo` éléments renvoyés dans `generatorArray` ou `generatedArray` par défaut incluent à la fois l’expéditeur et les enregistrements de ressource générés. Dans le cas d’un type de fichier PDF, ce comportement génère plusieurs copies non souhaitées de l’enregistrement de fichier PDF &quot;d’origine&quot; dans la réponse. Vous pouvez éliminer ce problème en ajoutant `generatedArray/items/originator` à `excludeFieldArray`. Vous pouvez également spécifier un explicite de champs de réponse que vous souhaitez inclure dans `responseFieldArray`.

## Exemples {#section-8946ea4b9cb94912a8408249c897f192}

L’exemple de base suivant est une demande de poignée du générateur pour une image extraite d’un PDF. Elle comprend une longueur `containerArray` de 1 avec un élément incluant le fichier `assetHandle` PDF.

**Request**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Réponse**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

L’inverse de l’exemple ci-dessus est le suivant :

**Request**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Réponse**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

Dans cet exemple, un groupe est ajouté à un  avec `groupHandleArray`. Cet exemple utilise un seul groupe.

**Request**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Réponse**

Aucune
