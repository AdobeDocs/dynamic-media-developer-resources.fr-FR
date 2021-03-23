---
description: Contient les paramètres du serveur de plate-forme.
seo-description: Contient les paramètres du serveur de plate-forme.
seo-title: server.xml
solution: Experience Manager
title: server.xml
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# server.xml{#server-xml}

Contient les paramètres du serveur de plate-forme.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, sans quoi le serveur de plateformes risque de ne pas se début.

Pour que les modifications prennent effet, le serveur de plateformes doit être redémarré après avoir modifié ce fichier.

Le diagramme suivant illustre les paramètres qui peuvent être modifiés dans ce fichier. Reportez-vous aux sections correspondantes plus haut dans ce document pour obtenir une description de ces paramètres. Notez que ce diagramme n&#39;est pas une représentation complète de [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

