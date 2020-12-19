---
description: Contient les paramètres de configuration d’Image Server.
seo-description: Contient les paramètres de configuration d’Image Server.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contient les paramètres de configuration d’Image Server.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, sans quoi le serveur d’images risque de ne pas se début.

Pour que les modifications prennent effet, redémarrez Image Server après avoir modifié ce fichier. Seules les valeurs d’élément répertoriées ci-dessous sont prises en charge pour modification. Modifiez tout autre contenu de ce fichier uniquement si le support technique de Scene7 vous en informe.

>[!NOTE]
>
>Ne modifiez pas la structure de `<imageserverregistry>`, y compris l&#39;ordre des éléments. Soyez prudent lors de la modification de ce fichier, sinon le serveur d’images risque de ne pas se début.

La figure suivante illustre les éléments qui peuvent être modifiés. D&#39;autres éléments sont présents et ne doivent pas être modifiés. L’ordre des éléments ci-dessous ne reflète pas l’ordre dans lequel ils doivent être présents dans le fichier.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Remarques {#section-7217f011f69f41e7af4f3983d7776d6f}

Plusieurs éléments `<RootPath>` peuvent être présents (un pour chaque dossier de fichier de données source). Image Server recherche les chemins d’accès racine dans l’ordre spécifié pour trouver un fichier source particulier.
