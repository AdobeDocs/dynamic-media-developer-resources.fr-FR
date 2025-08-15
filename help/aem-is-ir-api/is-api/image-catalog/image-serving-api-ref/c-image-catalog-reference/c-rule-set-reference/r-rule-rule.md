---
title: règle
description: Élément de règle de requête. Une ou plusieurs règles sont facultatives dans l’élément <ruleset>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fabd469-c80c-422a-80b0-3d31ce191d58
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 2%

---

# règle{#rule}

Élément de règle de requête. Une ou plusieurs règles sont facultatives dans l’élément `<ruleset>` .

## Attributs {#section-d4a3b0496c0c4aa5bd7da87203b9379b}

`OnMatch = "break" | "continue" | "error"` : facultatif. La valeur par défaut est « break ».

`Replace = "first" | "all"` : facultatif. La valeur par défaut est « first ».

`RequestType` = *»`types` »* : facultatif. Spécifie à quel contexte d&#39;entrée la règle s&#39;applique. *`types`* est une liste séparée par des virgules, qui peut inclure un ou plusieurs des jetons répertoriés dans le tableau suivant. Si `RequestType` cette option n’est pas spécifiée, la règle s’applique aux demandes reçues sur tous les contextes pris en charge.

<table id="table_4935E1ED03624DA6AF3F8DC9AAA10237"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><b>jeton</b> </p> </th> 
   <th class="entry"> <p><b>Contexte</b> </p> </th> 
   <th class="entry"> <p><b> Description </b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">'est </span> </p> </td> 
   <td> <p> <span class="filepath"> /is/image/</span> </p> </td> 
   <td> <p>Application aux demandes de diffusion d’images </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Ir</span> </p> </td> 
   <td> <p> <span class="filepath"> /ir/render/</span> </p> </td> 
   <td> <p>Appliqué aux demandes de rendu d’image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> statique</span> </p> </td> 
   <td> <p> <span class="filepath"> /is/content/</span> </p> </td> 
   <td> <p>Appliqué aux requêtes de contenu statique </p> </td> 
  </tr> 
 </tbody> 
</table>

**`Name = "text"`** : facultatif. Utilisé pour identifier l’élément dans les `<rule>` journaux de débogage et les messages d’erreur.

`  *`Attribut`* ="value"` : facultatif. `<rule>` Elements peut définir n’importe lequel des attributs suivants dans n’importe quelle combinaison. S’ils sont spécifiés et que la règle est correctement mise en correspondance, ils remplacent les attributs de catalogue correspondants pour cette demande. La valeur par défaut est `RequestType="is"`.

<table id="table_67AED5BEADDF4DAC99B5EF46438C1ABC"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <span class="varname"> Attribute </span> </b> </th> 
   <th class="entry"> <p>Attribut de catalogue d’images correspondant </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> DefaultImageMode</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782" type="reference" format="dita" scope="local"> attribute::DefaultImageMode</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> ErrorImage</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c" type="reference" format="dita" scope="local"> attribute::ErrorImage</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Expiration</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7" type="reference" format="dita" scope="local"> attribute::Expiration</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> MaxPix</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5" type="reference" format="dita" scope="local"> attribute::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RequestLock</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0" type="reference" format="dita" scope="local"> attribut ::RequestLock</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Demander l’obfuscation</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd" type="reference" format="dita" scope="local"> attribut ::RequestObfuscation</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> RootUrl</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rooturl.md#reference-3b0e43881020409cbe642366913cf137" type="reference" format="dita" scope="local"> attribut ::RootUrl</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> SavePath</span> </p> </td> 
   <td> <p> <a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-savepath.md#reference-9c4686dc153b41d8a0751cde83615432" type="reference" format="dita" scope="local"> attribut ::SavePath</a> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Filigrane</span> </p> </td> 
   <td> <p><a href="../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b" type="reference" format="dita" scope="local"> attribut ::Watermark</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Reportez-vous à la description de l’attribut de catalogue d’images correspondant pour plus de détails.

Les attributs Expiration remplacent uniquement les valeurs d’attribut par défaut. Le remplacement est ignoré si une valeur de `catalog::Expiration` spécifique s’applique à la requête.

## Données {#section-8fce013a4c724da58af3fee4e7a90e72}

<table id="simpletable_4F1C03671DA942A3A332B2C686A63C52"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;expression&gt;</span> </p></td> 
  <td class="stentry"> <p>Facultatif </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;substitution&gt;</span> </p></td> 
  <td class="stentry"> <p>Facultatif </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;addressfilter&gt;</span>&lt;/addressfilter&gt; </p></td> 
  <td class="stentry"> <p>Facultatif </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &lt;header&gt;</span>&lt;/header&gt; </p></td> 
  <td class="stentry"> <p>Facultatif </p></td> 
 </tr> 
</table>

## Remarques {#section-0c5fbc363070419d8c9800b0c02dc9f9}

Si `<expression>` et `<substitution>` sont spécifiés et que les sous-chaînes capturées ne sont pas utilisées, la première sous-chaîne correspondante est remplacée par `<substitution>`.

Si `<expression>` n’est pas spécifié, tout chemin correspond et `<substitution>` est ajouté à la fin du chemin.

Si `<substitution>` n’est pas spécifié, aucune transformation de chemin ou de requête ne se produit, mais tous les attributs de catalogue spécifiés sont remplacés. Si `<substitution>` est vide, la sous-chaîne correspondante est supprimée.

L’objet `<addressfilter>` est appliqué uniquement en cas de correspondance et avant l’application des règles de requête.
