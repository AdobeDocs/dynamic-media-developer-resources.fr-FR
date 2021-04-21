---
description: Utilisez ces paramètres de serveur pour enregistrer l’accès.
solution: Experience Manager
title: Journalisation des accès
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 3%

---


# Journalisation d&#39;accès {#access-logging}

Utilisez ces paramètres de serveur pour enregistrer l’accès.

Syntaxe

## TC::directory - Dossier de fichiers journaux {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Dossier dans lequel le serveur de plateformes écrit les fichiers journaux. Il peut s&#39;agir d&#39;un chemin absolu ou d&#39;un chemin relatif à *`install_folder`*. La valeur par défaut est [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que le dossier dispose des droits d’accès en lecture/écriture appropriés si Image Serving est installé pour être exécuté sous un compte utilisateur autre que root.

## TC::maxDays - Nombre de jours pour conserver les fichiers journaux {#section-45cbecffc5694c87b7d5c176a44a4885}

Le nombre de jours de fichiers journaux doit être conservé. De nouveaux fichiers journaux sont créés tous les jours à minuit. Actuellement, le serveur supprime tous les fichiers du dossier de fichiers journaux dont l’ancienneté est supérieure au nombre de jours spécifié, y compris ceux écrits par le serveur d’images ou le serveur de rendu. Valeur par défaut : 10.

## TC::prefix - Nom du fichier journal d&#39;accès {#section-1003856323b844049632710a5a056aa7}

Préfixe du nom du fichier dans lequel les données du journal d&#39;accès sont écrites. La date et le suffixe du fichier ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) sont ajoutés à la chaîne spécifiée. Le nom du fichier journal d&#39;accès doit être différent de celui du fichier journal de suivi. La valeur par défaut est &quot; `access-`&quot;.

## TC::pattern - Modèle de journal d&#39;accès {#section-22775ea85cee444d8a7d7336a3b1feef}

Spécifie le modèle de données pour les enregistrements du journal d&#39;accès à Platform Server. La chaîne de modèle spécifie les variables qui sont remplacées par leurs valeurs correspondantes. Tous les autres caractères de la chaîne de modèle sont transférés littéralement dans l’enregistrement du journal.

Pour utiliser l&#39;utilitaire de réchauffement du cache, les espaces doivent être utilisés comme séparateurs de champs. Le serveur de plateformes remplace tous les espaces et les caractères &quot;%&quot; dans les valeurs de champ par `%20` et `%25`, respectivement.

Les variables de modèle suivantes sont prises en charge :

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Motif</b> </th> 
   <th class="entry"> <b>Description</b> </th> 
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
   <td> <p>Nombre d'octets de réponse, à l'exclusion des en-têtes HTTP, ou ' si 0. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Nombre d’octets de réponse, à l’exception des en-têtes HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Temps de traitement de la demande en millisecondes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>id de thread (pour le référencement croisé des entrées de journal de débogage/d'erreur). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>date et heure, au format <span class="codeph"> <span class="varname"> aaaa </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span> : <span class="varname"> mm </span> : <span class="varname"> ss </span>. <span class="varname"> Décalage  </span> SSS  </span> </p> <p> ( <span class="varname"> SSS </span> sont msec, <span class="varname"> offset </span> est le décalage horaire GMT); la valeur de temps est capturée lorsque la réponse est envoyée au client. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Méthode de requête ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>, etc.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Chevauchement des requêtes (nombre de requêtes traitées simultanément). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Port local sur lequel cette demande a été reçue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Chaîne de requête (précédée d'un '?' s'il existe). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Première ligne de requête (méthode de requête, URI, version HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Identique à <span class="codeph"> %r </span>, mais applique un codage HTTP limité à l'URI pour éviter les problèmes d'analyse des journaux. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Code d’état de la réponse HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ID de session utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Date et heure, au format de journal commun. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Utilisateur distant qui a été authentifié (le cas échéant), sinon "". </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>chemin d’accès URI. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Nom du serveur local. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Temps de traitement de la demande en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>Clé de cache du serveur de plateformes (nom/dossier de fichier cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Mot clé de gestion du cache du serveur de plateformes : <span class="codeph"> { RÉUTILISÉ | CRÉÉ | MIS À JOUR | DISTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDÉE | IGNORÉ | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>Type MIME de la réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Contexte de destination si un contexte est avancé. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p>Valeur de l'en-tête de réponse <span class="codeph"> de l'balise </span> (signature MD5 des données de réponse). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>Message d’erreur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>Temps nécessaire pour récupérer l’entrée de cache ou les données du serveur Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>Temps nécessaire à l’analyse des demandes et à la recherche de catalogue d’images. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>Indique si cette requête a tenté un accès basé sur un chemin en dehors du système de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>Adresse IP du serveur homologue dans le cluster de cache qui a fourni l'entrée de cache ou "-" si <span class="codeph"> CacheUse </span> n'est ni <span class="codeph"> REMOTE_CREATED </span> ni <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>Catégorie d’erreur : </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0 = aucune erreur. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=image(s) introuvable(s) sur le serveur. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2 = Erreur d’utilisation du protocole IS ou erreur de contenu autre que 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3 = autre erreur du serveur. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4 = demande refusée en raison d’une surcharge temporaire du serveur. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p>Valeur majuscule de <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>ID racine du catalogue principal de la demande. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>Temps nécessaire au serveur de plateformes pour envoyer une réponse après avoir écrit des données dans le flux de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p>Comme <span class="codeph"> %B </span>, mais inclut des valeurs pour les réponses 304 (non modifiées). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r  </span> </p> </td> 
   <td> <p>URL finale après toutes les transformations d’ensembles de règles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>Valeur de l’en-tête de requête HTTP spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>Valeur de l’en-tête de réponse HTTP spécifié. </p> </td> 
  </tr> 
 </tbody> 
</table>

Valeur par défaut : `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
