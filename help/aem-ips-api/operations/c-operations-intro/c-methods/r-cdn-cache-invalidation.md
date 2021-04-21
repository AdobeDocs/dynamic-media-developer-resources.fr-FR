---
description: Transfère la liste d’URL fournie au fournisseur Dynamic Media CDN (Content Distribution Network) pour invalider le cache existant de réponses HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 4%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Transfère la liste d’URL fournie au fournisseur Dynamic Media CDN (Content Distribution Network) pour invalider le cache existant de réponses HTTP.

## cdnCacheInvalidation : À propos de {#section-4f70d2bc79d64288b961836ab17e9690}

L’invalidation du cache CDN force toutes les requêtes HTTP pour que ces URL soient revalidées par rapport aux données actuellement publiées sur le réseau Dynamic Media après le traitement de cette demande d’invalidation par le réseau CDN. Toute URL qui n’est pas connectée à la structure d’URL du service Dynamic Media et qui correspond directement à l’ID racine de la société Dynamic Media attribué lors de la création de la société entraîne une erreur d’API pour l’ensemble de la requête. Toute URL non valide que le CDN ne prend pas en charge et qu’il considère comme non valide entraîne également une erreur d’API pour l’ensemble de la requête.

**Fréquence d&#39;utilisation : Règles**

Les règles régissant la fréquence d’utilisation de cette fonction sont contrôlées par les partenaires CDN de Contenu multimédia dynamique. Le CDN conserve le pouvoir discrétionnaire de dégrader la réactivité de ces invalidations afin de maintenir les performances optimales de son service à ses utilisateurs. Si Dynamic Media est averti d&#39;une utilisation excessive de cette fonctionnalité, nous devrons recourir à la désactivation de la fonctionnalité, soit par société, soit entièrement sur l&#39;ensemble du service.

**Courriers électroniques de confirmation**

Les courriers électroniques de confirmation du partenaire CDN Dynamic Media peuvent être envoyés à l’auteur de la liste ou à 5 autres adresses électroniques. L’API envoie la confirmation lorsque l’ensemble du réseau CDN a été averti que les URL référencées dans le courrier électronique ont été effacées. Un appel unique à `cdnCacheInvalidation` peut envoyer plusieurs courriers électroniques si le nombre d’URL fournies dépasse le nombre que Dynamic Media peut fournir au partenaire CDN sur une seule notification. Actuellement, cela se produit si la requête dépasse 100 URL, mais est susceptible d’être modifiée à la demande du partenaire CDN.

**Pris en charge depuis**

6,0

## Types d&#39;utilisateur autorisés {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Paramètres {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

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
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Le handle vers la société connectée aux URL à invalider. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types : UrlArray</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Liste de 1 000 URL au maximum à invalider à partir du cache CDN. Toutes les URL doivent contenir l'ID racine de la société Dynamic Media à invalider. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>Poignée faisant référence à la demande de purge. </p> <p>L'API <span class="codeph"> cdnCacheInvalidation</span> invalide désormais le cache presque immédiatement (~5 secondes). Ainsi, l’interrogation du statut d’invalidation n’est généralement plus requise. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimationSecondes</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Estimation des secondes avant la fin de la demande de purge. Les clients doivent attendre cette heure avant d’obtenir le statut de vote. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-f414361a58e84dfcbbac30a358d02125}

Cet exemple demande que quatre URL soient invalidées dans le cache CDN. La réponse contient des comptes récapitulatifs du succès des opérations et une liste des détails d&#39;erreur fournis directement par le CDN pour aider le client à utiliser cette fonctionnalité.

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

