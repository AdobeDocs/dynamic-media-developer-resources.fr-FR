---
description: 'null'
seo-description: 'null'
seo-title: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic media
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Le modèle d’URL du serveur d’informations permet de récupérer les paires clé/valeur pour la substitution de variable dans le modèle de contenu du panneau d’informations. Le modèle spécifié contient généralement des espaces réservés aux macros qui sont remplacés par les données réelles avant l’envoi de la requête au serveur. </p> <p><span class="codeph"> $1$</span> est remplacé par la valeur de survol qui a déclenché l’ de  <span class="codeph"> InfoPanelPopup</span> . </p> <p><span class="codeph"> $2$</span> est remplacé par le numéro de séquence de l’image active dans la visionneuse d’images. </p> <p><span class="codeph"> $3$</span> est remplacé par le premier élément de chemin spécifié dans le nom du jeu parent de l’élément actif. Il correspond généralement à l’ID de catalogue. </p> <p><span class="codeph"> $4$</span> est remplacé par l’élément suivant dans le chemin d’accès et correspond à l’ID de ressource. La syntaxe de requête du serveur d’informations est dépendante du serveur d’informations et diffère d’un serveur à l’autre. Par exemple, voici un modèle type de requête de serveur d’informations Scene7 : </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Sachez que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code HTML et ce code JavaScript sont sécurisés.

## Propriétés {#section-71356e3c13244e62b0582980d9d05328}

Facultatif.

## Par défaut {#section-22e9af803f724434807d34e200eb7518}

Aucune

## Exemple {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
