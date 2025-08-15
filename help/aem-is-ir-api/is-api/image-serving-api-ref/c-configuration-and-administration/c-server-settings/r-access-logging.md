---
description: Utilisez ces paramètres de serveur pour l’accès à la journalisation.
solution: Experience Manager
title: Journalisation des accès
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Journalisation des accès{#access-logging}

Utilisez ces paramètres de serveur pour l’accès à la journalisation.

Syntaxe

## TC ::d irectory - Dossier de fichiers journaux {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Le dossier dans lequel l’écrit les [!DNL Platform Server] fichiers journaux. Il peut s’agir d’un chemin absolu ou d’un chemin relatif à *`install_folder`*. La valeur par défaut est [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>Le nouveau dossier doit être créé avant de modifier ce paramètre. Assurez-vous que le dossier dispose des privilèges d’accès en lecture/écriture appropriés si Image Serving est installé pour s’exécuter sous un compte d’utilisateur autre que root.

## TC ::maxDays - nombre de jours de conservation des fichiers journaux {#section-45cbecffc5694c87b7d5c176a44a4885}

Le nombre de jours pendant lesquels les fichiers journaux doivent être conservés. De nouveaux fichiers journaux sont créés chaque jour à minuit. À ce stade, le serveur supprime tous les fichiers du dossier de fichiers journaux qui sont antérieurs au nombre de jours spécifié, y compris ceux écrits par le serveur d’images ou le serveur de rendu. Par défaut : 10.

## TC ::p refix - Nom du fichier journal d’accès {#section-1003856323b844049632710a5a056aa7}

Préfixe de nom pour le fichier dans lequel les données du journal d’accès sont écrites. La date et le suffixe de fichier ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) sont ajoutés à la chaîne spécifiée. Le nom du fichier journal d’accès doit être différent de celui du fichier journal de suivi. La valeur par défaut est « `access-` ».

## TC::pattern - Modèle de journal d&#39;accès {#section-22775ea85cee444d8a7d7336a3b1feef}

Indique le modèle de données pour les enregistrements du journal d’accès [!DNL Platform Server]. La chaîne de modèle spécifie les variables qui sont remplacées par leurs valeurs correspondantes. Tous les autres caractères de la chaîne de modèle sont littéralement transférés vers l’enregistrement du journal.

Pour utiliser l’utilitaire de préchauffage du cache, les espaces doivent être utilisés comme séparateurs de champs. Le [!DNL Platform Server] remplace tous les espaces et les caractères « % » dans les valeurs de champ par `%20` et `%25`, respectivement.

Les variables de schéma ci-dessous sont prises en charge :

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Modèle</b> </th> 
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
   <td> <p>Nombre d’octets de réponse excluant les en-têtes HTTP ou ' ' si zéro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Nombre d’octets de réponse excluant les en-têtes HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Temps de traitement de la demande en millisecondes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>Thread ID (pour le référencement croisé des entrées du journal de débogage/d’erreur). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>date et heure, au format <span class="codeph"> aaaa <span class="varname">- </span> MM <span class="varname">- </span> jj <span class="varname"> </span> HH <span class="varname">: </span> mm <span class="varname">: </span> ss <span class="varname">.</span> <span class="varname">Décalage SSS </span></span> </p> <p> <span class="varname">( SSS </span> sont msec, <span class="varname"> le décalage </span> est le décalage temporel GMT) ; la valeur temporelle est capturée lorsque la réponse est envoyée au client. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Méthode de requête ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>, etc.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %o </span> </p> </td> 
   <td> <p>Chevauchement des demandes (nombre de demandes traitées simultanément). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Port local sur lequel cette demande a été reçue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Chaîne de requête (précédée d'un '?' s’il existe). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Première ligne de requête (méthode de requête, URI, version HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Identique à <span class="codeph"> %r </span>, mais applique un codage HTTP limité à l’URI pour éviter les problèmes d’analyse du journal. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Code d’état de réponse HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>ID de session utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Date et heure, dans le format de journal courant. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Utilisateur distant authentifié (le cas échéant), sinon ''. </p> </td> 
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
   <td> <p>[!DNL Platform Server] Clé du cache (dossier/nom du fichier cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] Mot clé de gestion de la mémoire cache : <span class="codeph"> { REUSED | CRÉÉ | MIS À JOUR | À DISTANCE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDÉ | IGNORÉ | NON DÉFINI } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>Type MIME de réponse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Contexte de destination si un contexte de transfert se produit. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>Valeur <span class="codeph"> de l’en-tête de réponse etag </span> (signature MD5 des données de réponse). </p> </td> 
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
   <td> <p>Indique si cette demande a tenté ou non un accès basé sur le chemin en dehors du système de catalogue. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>Adresse IP du serveur homologue dans le cluster de cache qui a fourni l’entrée de cache ou '-' si <span class="codeph"> CacheUse </span> n’est ni <span class="codeph"> REMOTE_CREATED </span> ni <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Catégorie d’erreur : </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=Aucune erreur. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=Image(s) introuvable(s) sur le serveur. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2 = Erreur d’utilisation du protocole IS ou une erreur de contenu autre que 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3 = Autre erreur de serveur. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=Demande refusée en raison d’une surcharge temporaire du serveur. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>Valeur majuscule de <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>ID racine du catalogue principal de la requête. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>Temps nécessaire [!DNL Platform Server] pour envoyer une réponse après avoir écrit des données dans le flux de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Comme <span class="codeph"> %B </span>, mais inclut des valeurs pour les réponses 304 (non modifiées). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>URL finale après toutes les transformations liées au jeux de règles. </p> </td> 
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
