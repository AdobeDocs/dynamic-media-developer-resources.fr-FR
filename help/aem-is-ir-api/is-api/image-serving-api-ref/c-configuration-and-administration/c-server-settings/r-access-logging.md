---
description: Utilisez ces paramètres de serveur pour l’accès à la journalisation.
solution: Experience Manager
title: Journalisation des accès
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
TQID: 'https://experienceleague.adobe.com/YY1vKXzVCe8TRK0lYsdkH5ds5EHCGkBOz1TaMx5IMi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 681
ht-degree: 0%

---

# Journalisation des accès{#access-logging}

Utilisez ces paramètres de serveur pour l’accès à la journalisation.

Syntaxe

## TC::directory - Dossier du fichier journal {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Dossier dans lequel le [!DNL Platform Server] écrit les fichiers journaux. Il peut s’agir d’un chemin absolu ou d’un chemin relatif à *`install_folder`*. La valeur par défaut est [!DNL &#x200B; *`install_folder`*/logs].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que le dossier dispose des privilèges d’accès en lecture/écriture appropriés si le service d’images est installé pour s’exécuter sous un compte utilisateur autre que root.

## TC::maxDays - Nombre de jours de conservation des fichiers journaux {#section-45cbecffc5694c87b7d5c176a44a4885}

Le nombre de jours pendant lesquels les fichiers journaux doivent être conservés De nouveaux fichiers journaux sont créés tous les jours à minuit. À ce stade, le serveur supprime tous les fichiers du dossier de fichiers journaux qui sont plus anciens que le nombre de jours spécifié, y compris ceux écrits par le serveur d’images ou le serveur de rendu. La valeur par défaut est 10.

## TC::prefix - Nom du fichier journal d&#39;accès {#section-1003856323b844049632710a5a056aa7}

Préfixe du nom du fichier dans lequel les données du journal d’accès sont écrites. La date et le suffixe du fichier ( [!DNL &#x200B; *`yyyy`*-*`mm`*-*`dd`*.log]) sont ajoutés à la chaîne spécifiée. Le nom du fichier journal d’accès doit être différent de celui du fichier journal de suivi. La valeur par défaut est « `access-` ».

## TC::pattern - Modèle de journal d&#39;accès {#section-22775ea85cee444d8a7d7336a3b1feef}

Indique le modèle de données pour les enregistrements du journal d’accès [!DNL Platform Server]. La chaîne de modèle spécifie les variables qui sont remplacées par leurs valeurs correspondantes. Tous les autres caractères de la chaîne de modèle sont littéralement transférés vers l’enregistrement du journal.

Pour utiliser l’utilitaire de préchauffage du cache, les espaces doivent être utilisés comme séparateurs de champs. Le [!DNL Platform Server] remplace tous les espaces et les caractères « % » dans les valeurs de champ par `%20` et `%25`, respectivement.

Les variables de modèle suivantes sont prises en charge :

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Motif</b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>Adresse IP distante. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>Adresse IP locale. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>Nombre d'octets de réponse hors en-têtes HTTP ou ' ' si zéro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Nombre d’octets de réponse à l’exclusion des en-têtes HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Temps de traitement de la demande en millisecondes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>id de thread (pour le référencement croisé des entrées du journal de débogage/erreur). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>date et heure, au format <span class="codeph"> <span class="varname"> aaaa </span>- <span class="varname"> MM </span>- <span class="varname"> jj </span> <span class="varname"> HH </span> : <span class="varname"> mm </span> : <span class="varname"> </span> <span class="varname">. </span> de décalage de </span> SSS </p> <p> (<span class="varname"> </span> SSS sont des ms, <span class="varname"> décalage </span> est le décalage horaire GMT) ; la valeur temporelle est capturée lorsque la réponse est envoyée au client. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Méthode de requête ( </span> <span class="codeph"> GET, </span> POST <span class="codeph">, etc.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Chevauchement des demandes (nombre de demandes traitées simultanément). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Port local sur lequel cette demande a été reçue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Chaîne de requête (précédée d'un '?' si elle existe). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Première ligne de la requête (méthode de requête, URI, version HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Identique à <span class="codeph"> %r </span>, mais applique un codage HTTP limité à l’URI pour éviter les problèmes d’analyse du journal. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Code de statut de la réponse HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ID de session de l’utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Date et heure, au format de journal courant. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Utilisateur distant qui a été authentifié (le cas échéant), sinon ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>Chemin URI. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Nom du serveur local. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Temps de traitement de la requête en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] clé de cache (nom/dossier du fichier cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] mot-clé de gestion du cache : <span class="codeph"> { REUSED | CREATED | UPDATED | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDATED | IGNORED | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>Type MIME de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Contexte de destination si un transfert de contexte se produit. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>La valeur de l’en-tête de réponse <span class="codeph"> etag </span> (signature MD5 des données de réponse). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>Message d’erreur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Temps nécessaire pour récupérer l’entrée du cache ou les données du serveur d’images. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>Temps nécessaire à l’analyse des requêtes et à la recherche du catalogue d’images. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>Indique si cette requête a tenté ou non un accès basé sur un chemin en dehors du système de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>Adresse IP du serveur homologue dans le cluster de cache qui a délivré l'entrée de cache ou '-' si <span class="codeph">'</span> CacheUse n'est ni <span class="codeph"> REMOTE_CREATED </span> ni <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Catégorie d’erreur : </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=aucune erreur. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=image(s) introuvable(s) sur le serveur. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=Erreur d'utilisation du protocole IS ou erreur de contenu autre que 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=autre erreur de serveur. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=demande refusée en raison d’une surcharge temporaire du serveur. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>Valeur en majuscules de <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>ID racine du catalogue principal de la requête. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>Temps nécessaire [!DNL Platform Server] envoyer une réponse après l’écriture de données dans le flux de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Comme <span class="codeph"> %B </span>, mais inclut des valeurs pour les réponses 304 (non modifiées). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformUrl}r </span> </p> </td> 
   <td> <p>URL finale après toutes les transformations de l’ensemble de règles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>Valeur de l’en-tête de requête HTTP spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>Valeur de l’en-tête de réponse HTTP spécifié. </p> </td> 
  </tr> 
 </tbody> 
</table>

La valeur par défaut est `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
