---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>Le modèle d’URL du serveur d’informations est utilisé pour récupérer les paires clé/valeur pour la substitution de variable dans le modèle de contenu du panneau d’informations. Le modèle spécifié contient généralement des espaces réservés de macro qui sont remplacés par les données réelles avant l’envoi de la demande au serveur. </p> <p><span class="codeph"> $1$</span> est remplacé par la valeur de survol qui a déclenché l’activation <span class="codeph"> InfoPanelPopup</span>. </p> <p><span class="codeph"> $2$</span> est remplacé par le numéro de séquence de l’image actuelle dans la visionneuse d’images. </p> <p><span class="codeph"> $3$</span> est remplacé par le premier élément de chemin spécifié dans le nom de l’ensemble parent de l’élément actuel. Il correspond généralement à l’ID de catalogue. </p> <p><span class="codeph"> $4$</span> est remplacé par l’élément suivant dans le chemin d’accès et correspond à l’identifiant de la ressource. La syntaxe de la requête du serveur d’informations est dépendante du serveur d’informations et elle diffère d’un serveur à l’autre. Par exemple, voici un modèle de demande de serveur d’informations Dynamic Media type : </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gardez à l’esprit que lorsque vous configurez la fenêtre contextuelle du panneau d’informations, le code d’HTML et le code JavaScript transmis au panneau d’informations s’exécutent sur l’ordinateur du client. Par conséquent, assurez-vous que ce code d’HTML et ce code JavaScript sont sécurisés.

## Propriétés {#section-71356e3c13244e62b0582980d9d05328}

Facultatif.

## Par défaut {#section-22e9af803f724434807d34e200eb7518}

Aucune

## Exemple {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
