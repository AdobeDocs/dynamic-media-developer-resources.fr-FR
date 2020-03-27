---
description: Transfère le d’URL fourni au fournisseur CDN (Content Distribution Network) Scene7 pour invalider le cache existant des réponses HTTP.
seo-description: Transfère le d’URL fourni au fournisseur CDN (Content Distribution Network) Scene7 pour invalider le cache existant des réponses HTTP.
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Transfère le d’URL fourni au fournisseur CDN (Content Distribution Network) Scene7 pour invalider le cache existant des réponses HTTP.

## cdnCacheInvalidation : À propos de {#section-4f70d2bc79d64288b961836ab17e9690}

L’invalidation du cache CDN force toutes les requêtes HTTP de ces URL à être revalidées par rapport aux données publiées actuelles sur le réseau Scene7 une fois cette demande d’invalidation traitée via le réseau CDN. Toute URL qui n’est pas connectée à la structure d’URL du service Scene7 et qui correspond directement à l’ID racine du Scene7 attribué lors de la création du entraîne une erreur d’API pour l’ensemble de la requête. Toute URL non valide que le CDN ne prend pas en charge et qu’il considère comme non valide entraînera également une erreur d’API pour l’ensemble de la requête.

**Fréquence d&#39;utilisation : Règles**

Les règles régissant la fréquence d’utilisation de cette fonction sont contrôlées par les partenaires CDN de Scene7. Le CDN conserve le pouvoir discrétionnaire de dégrader la réactivité de ces invalidations afin de maintenir les performances optimales de son service à ses utilisateurs. Si Scene7 est averti de l’utilisation excessive de cette fonctionnalité, nous devrons recourir à la désactivation de cette dernière, soit  par, soit dans l’ensemble du service.

**Courriers électroniques de confirmation**

Les courriers électroniques de confirmation du partenaire CDN Scene7 peuvent être envoyés au créateur de l’ ou à 5 autres adresses électroniques. L’API envoie la confirmation lorsque l’ensemble du réseau CDN a été informé que les URL référencées dans le courrier électronique ont été effacées. Un appel unique à `cdnCacheInvalidation` peut envoyer plusieurs courriers électroniques si le nombre d’URL fournies dépasse le nombre que Scene7 peut envoyer au partenaire CDN sur une seule notification. À l’heure actuelle, cela se produirait si la requête dépasse 100 URL, mais est sujette à modification à la demande du partenaire CDN.

**Pris en charge depuis**

6.0

## Types d’utilisateurs autorisés {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Paramètres {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nom</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Obligatoire</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> sociétéHandle</span></span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Le nom d’utilisateur du associé aux URL à invalider. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span></span> </p> </td> 
   <td> <p> <span class="codeph"> type:UrlArray</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p>  d’un maximum de 1 000 URL à invalider à partir du cache CDN. Toutes les URL doivent contenir l’ID racine du Scene7  invalidé. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nom</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Obligatoire</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Handle référençant la demande de purge. </p> <p>L’API <span class="codeph"> cdnCacheInvalidation</span> invalide désormais le cache presque immédiatement (~5 secondes). Ainsi, l’interrogation du statut d’invalidation n’est généralement plus nécessaire. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimationSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Durée estimée en secondes avant la fin de la demande de purge. Les clients doivent attendre cette fois-ci avant d’interroger le statut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-f414361a58e84dfcbbac30a358d02125}

Cet exemple demande que quatre URL soient invalidées dans le cache CDN. La réponse contient un résumé du nombre de réussites des opérations et un de détails d’erreur fournis directement par le CDN pour aider le client à utiliser cette fonctionnalité.

`getCdnCacheInvalidationStatus` opération.

**Request**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Réponse**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

