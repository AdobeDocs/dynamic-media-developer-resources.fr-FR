---
description: Transfère la liste fournie d’URL au fournisseur Dynamic Media CDN (Content Distribution Network) pour invalider le cache existant de réponses HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

Transfère la liste fournie d’URL au fournisseur Dynamic Media CDN (Content Distribution Network) pour invalider le cache existant de réponses HTTP.

## cdnCacheInvalidation : à propos {#section-4f70d2bc79d64288b961836ab17e9690}

L’invalidation du cache CDN force toutes les requêtes HTTP pour que ces URL soient revalidées par rapport aux données publiées actuelles sur le réseau Dynamic Media après le traitement de cette demande d’invalidation par le biais du réseau CDN. Toute URL qui n’est pas connectée à la structure d’URL du service Dynamic Media et qui correspond directement à l’ID racine de l’entreprise Dynamic Media affecté lors de la création de l’entreprise entraîne une erreur d’API pour l’ensemble de la requête. Toute URL non valide que le réseau de diffusion de contenu ne prend pas en charge et qu’il considère comme non valide entraîne également une erreur d’API pour l’ensemble de la requête.

**Fréquence d’utilisation : règles**

Les règles régissant la fréquence d’utilisation de cette fonctionnalité sont contrôlées par les partenaires CDN de Dynamic Media. Le réseau de diffusion de contenu conserve la discrétion de dégrader la réactivité de ces invalidations afin de maintenir des performances optimales de son service à ses utilisateurs. Si Dynamic Media est averti de l’utilisation abusive de cette fonctionnalité, l’Adobe doit recourir à la désactivation de cette fonction pour chaque entreprise ou entièrement pour l’ensemble du service.

**Courriers électroniques de confirmation**

Les emails de confirmation du partenaire Dynamic Media CDN peuvent être envoyés à l’auteur de la liste ou à 5 autres adresses électroniques au maximum. L’API envoie la confirmation lorsque l’ensemble du réseau CDN a été informé que les URL référencées dans l’email ont été effacées. Un seul appel à `cdnCacheInvalidation` peut envoyer plusieurs emails si le nombre d’URL fournies dépasse le nombre que Dynamic Media peut fournir au partenaire CDN sur une seule notification. Actuellement, cela se produit si la requête dépasse 100 URL, mais qu’elle peut être modifiée sur la base de la requête du partenaire CDN.

**Pris en charge depuis**

6,0

## Types d’utilisateurs autorisés {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Paramètres {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Entrée** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
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
   <td> <p> Gestionnaire de la société connectée à l’URL à invalider. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types : UrlArray</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Liste de 1 000 URL au maximum à invalider à partir du cache CDN. Toutes les URL doivent contenir l’ID racine de la société Dynamic Media à invalider. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
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
   <td colname="col4"> <p>Gestionnaire référençant la requête de purge. </p> <p>L’API <span class="codeph"> cdnCacheInvalidation</span> invalide désormais le cache presque immédiatement (~5 secondes). Par conséquent, l’interrogation de l’état d’invalidation n’est généralement plus nécessaire. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Durée estimée en secondes jusqu’à la fin de la requête de purge. Les clients doivent attendre cette période avant d’interroger le statut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-f414361a58e84dfcbbac30a358d02125}

Cet exemple demande l’invalidation de quatre URL dans le cache CDN. La réponse contient un résumé des résultats des opérations et une liste des détails d’erreur fournis directement par le réseau de diffusion de contenu pour aider le client à utiliser cette fonctionnalité.

Opération `getCdnCacheInvalidationStatus`.

**Requête**

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
