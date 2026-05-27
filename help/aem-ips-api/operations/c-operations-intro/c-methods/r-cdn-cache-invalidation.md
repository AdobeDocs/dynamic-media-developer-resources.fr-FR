---
description: Transfère la liste d’URL fournie au fournisseur de réseau CDN (Content Distribution Network) Dynamic Media pour invalider son cache existant de réponses HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
TQID: 'https://experienceleague.adobe.com/EiiTKlBO9it1WQXYW2ed-4Vo5qi2YSlR2SageNHMUqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 472
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

Transfère la liste d’URL fournie au fournisseur de réseau CDN (Content Distribution Network) Dynamic Media pour invalider son cache existant de réponses HTTP.

## cdnCacheInvalidation : à propos {#section-4f70d2bc79d64288b961836ab17e9690}

L’invalidation du cache du réseau de diffusion de contenu force toutes les requêtes HTTP pour ces URL à être revalidées par rapport aux données publiées actuelles sur le réseau Dynamic Media une fois que cette requête d’invalidation a été traitée via le réseau CDN. Toutes les URL qui ne sont pas connectées à la structure d’URL du service Dynamic Media et qui correspondent directement à l’ID racine de société Dynamic Media affecté lorsque la société est créée entraînent une erreur d’API pour l’ensemble de la requête. Toute URL non valide que le réseau CDN ne prend pas en charge et qu’il considère comme non valide entraîne également une erreur d’API pour l’ensemble de la requête.

**Fréquence d’utilisation : règles**

Les règles régissant la fréquence d’utilisation de cette fonctionnalité sont contrôlées par les partenaires de réseau CDN de Dynamic Media. Le réseau CDN conserve la discrétion de dégrader la réactivité de ces invalidations afin de maintenir des performances optimales de son service pour ses utilisateurs. Si Dynamic Media est averti d’une utilisation excessive de cette fonctionnalité, Adobe doit désactiver cette fonctionnalité par société ou entièrement sur l’ensemble du service.

**E-mails de confirmation**

Les e-mails de confirmation du partenaire de réseau CDN Dynamic Media peuvent être envoyés au créateur de la liste ou à jusqu’à 5 autres adresses e-mail. L’API envoie la confirmation lorsque l’ensemble du réseau CDN a été averti que les URL référencées dans l’e-mail ont été effacées. Un seul appel à `cdnCacheInvalidation` peut envoyer plusieurs e-mails si le nombre d’URL fournies dépasse le nombre que Dynamic Media peut diffuser au partenaire de réseau CDN sur une seule notification. Actuellement, cela se produit si la requête dépasse 100 URL, mais peut être modifiée à la demande du partenaire de réseau CDN.

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
   <th class="entry"> <b> Name </b> </th> 
   <th class="entry"> Type de </b> <b></th> 
   <th class="entry"> <b> obligatoire</b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Identifiant de la société connectée aux URL à invalider. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> types :UrlArray</span> </p> </td> 
   <td> <p> Oui </p> </td> 
   <td> <p> Liste de 1 000 URL maximum à invalider à partir du cache du réseau CDN. Toutes les URL doivent contenir l’identifiant racine de la société Dynamic Media pour être invalidées. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name </b> </th> 
   <th class="entry"> Type de </b> <b></th> 
   <th class="entry"> <b> obligatoire</b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Un handle référençant la requête de purge. </p> <p>L’API <span class="codeph"> cdnCacheInvalidation</span> invalide désormais le cache presque immédiatement (~5 secondes). Par conséquent, l’interrogation pour le statut d’invalidation n’est généralement plus nécessaire. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Estimation du nombre de secondes avant la fin de la demande de purge. Les clients doivent attendre cette durée avant d’interroger le statut. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-f414361a58e84dfcbbac30a358d02125}

Cet exemple demande que quatre URL soient invalidées dans le cache du réseau CDN. La réponse contient un résumé des résultats des opérations et une liste des détails de l’erreur fournis directement par le réseau CDN pour aider le client à utiliser cette fonctionnalité.

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
