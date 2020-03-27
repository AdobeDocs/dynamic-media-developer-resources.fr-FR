---
description: Supprimez la sortie d’une tâche.
seo-description: Supprimez la sortie d’une tâche.
seo-title: batchjobdelete
solution: Experience Manager
title: batchjobdelete
topic: Scene7 Image Serving - Image Rendering API
uuid: d19ed1c8-e13b-4da4-90e3-6bb0dcce2a12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchjobdelete{#batchjobdelete}

Supprimez la sortie d’une tâche.

Si une tâche est en cours d’exécution, elle est immédiatement arrêtée et toutes ses informations de traitement sont supprimées. Si la tâche s’est terminée avec succès, son fichier de sortie est supprimé.

Ce paramètre :

<table id="simpletable_AACB976615FF4888A0816328DC48DCA3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> jobid</span> </p> </td> 
  <td class="stentry"> <p>ID de tâche obtenu au moment de l’envoi. </p></td> 
 </tr> 
</table>

Renvoie :

Statut de la tâche au moment de la réception de la demande de suppression, erreur si `jobid` elle est incorrecte ou si la tâche a déjà été supprimée.

## Exemple {#section-e0df8fc8e6554ba58e1fa937b8241ecf}

[!DNL http://scene7.adobe.com:8080/is/agm/AcmeCorp?req=batchjobdelete&jobid=1005907604914d8eb63126b98f7172n76a5]
