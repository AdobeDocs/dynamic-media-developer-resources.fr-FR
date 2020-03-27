---
description: Contient les paramètres du serveur de plateformes.
seo-description: Contient les paramètres du serveur de plateformes.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# server.xml{#server-xml}

Contient les paramètres du serveur de plateformes.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, sans quoi le serveur de plateformes risque de ne pas .

Pour que les modifications prennent effet, le serveur de plateformes doit être redémarré après avoir modifié ce fichier.

Le diagramme suivant illustre les paramètres qui peuvent être modifiés dans ce fichier. Reportez-vous aux sections correspondantes plus tôt dans ce  pour obtenir une description de ces paramètres. Notez que ce diagramme n&#39;est pas une représentation complète de [!DNL server.xml].

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

