---
description: Transfère la liste d’URL fournie au fournisseur Dynamic Media CDN (Content Distribution Network) pour invalider leur cache existant de réponses HTTP.
solution: Experience Manager
title: Invalidation cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# Invalidation cdnCacheInvalidation{#cdncacheinvalidation}

Transfère la liste d’URL fournie au fournisseur Dynamic Media CDN (Content Distribution Network) pour invalider leur cache existant de réponses HTTP.

## cdnCacheInvalidation : à propos {#section-4f70d2bc79d64288b961836ab17e9690}

L’invalidation du cache CDN force toutes les requêtes HTTP pour ces URL à être revalidées par rapport aux données publiées actuelles sur le réseau Dynamic Media une fois cette demande d’invalidation traitée via le réseau CDN. Toutes les URL qui ne sont pas connectées à la structure d’URL du service Dynamic Media et qui correspondent directement à l’ID racine d’entreprise Dynamic Media attribué lors de la création de l’entreprise entraînent une erreur d’API pour l’ensemble de la demande. Toute URL non valide que le CDN ne prend pas en charge et qu’il considère comme non valides entraîne également une erreur d’API pour l’ensemble de la demande.

**Fréquence d’utilisation : règles**

Les règles régissant la fréquence d’utilisation de cette fonctionnalité sont contrôlées par les partenaires CDN de Dynamic Media. Le CDN conserve le pouvoir discrétionnaire de dégrader la réactivité de ces invalidations afin de maintenir une performance optimale de son service à ses utilisateurs. Si Dynamic Media être informé d’une utilisation excessive de cette fonctionnalité, Adobe devez recourir à la désactivation de la fonctionnalité par entreprise ou entièrement sur l’ensemble du service.

**E-mails de confirmation**

Les e-mails de confirmation du partenaire CDN Dynamic Media peuvent être envoyés au créateur de la liste ou jusqu’à 5 autres adresses e-mail. L’API envoie la confirmation lorsque l’ensemble du réseau CDN a été informé que les URL référencées dans l’e-mail ont été effacées. Un seul appel à `cdnCacheInvalidation` peut envoyer plusieurs e-mails si le nombre d’URL fournies dépasse le nombre que Dynamic Media pouvez remettre au partenaire CDN sur une seule notification. Actuellement, c’est le cas si la demande dépasse 100 URL, mais est susceptible d’être modifiée à la demande du partenaire CDN.

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
   <th class="entry"> <b> Nom</b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Obligatoire</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"><span class="varname"> CompanyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Indiquez le handle de l’entreprise connectée aux URL à invalider. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"><span class="varname"> Tableau d’url</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types :UrlArray</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Liste proposant jusqu’à 1000 URL à invalider à partir du cache CDN. Toutes les URL doivent contenir l’ID racine Dynamic Media de l’entreprise à invalider. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output** ( `cdnCacheInvalidationReturn`)

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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> InvalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée faisant référence à la requête de purge. </p> <p>L’API <span class="codeph"> cdnCacheInvalidation</span> invalide désormais le cache presque immédiatement (~5 secondes). Par conséquent, l’interrogation pour l’état d’invalidation n’est généralement plus nécessaire. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Secondes estimées</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :int</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Estimation du nombre de secondes avant la fin de la demande de purge. Les clients doivent attendre cette heure avant d’interroger l’état. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-f414361a58e84dfcbbac30a358d02125}

Cet exemple demande l’annulation de quatre URL dans le cache CDN. La réponse contient des résumés du succès des opérations et une liste de détails d’erreur fournis directement à partir du CDN pour aider le client à utiliser cette fonctionnalité.

`getCdnCacheInvalidationStatus` opération.

**Demander**

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
