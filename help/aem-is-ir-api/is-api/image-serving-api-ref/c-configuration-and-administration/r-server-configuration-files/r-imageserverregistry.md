---
description: Contient les paramètres de configuration du serveur d’images.
seo-description: Contient les paramètres de configuration du serveur d’images.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Scene7 Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contient les paramètres de configuration du serveur d’images.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, faute de quoi le serveur d’images risque de ne pas .

Pour que les modifications prennent effet, redémarrez Image Server après avoir modifié ce fichier. Seules les valeurs d’élément répertoriées ci-dessous sont prises en charge pour modification. Modifiez tout autre contenu de ce fichier uniquement si l’assistance technique de Scene7 vous le conseille.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Ne modifiez pas la structure de `<imageserverregistry>`, y compris l’ordre des éléments. Soyez prudent lorsque vous modifiez ce fichier, sinon le serveur d’images risque de ne pas .

Le tableau suivant illustre les éléments qui peuvent être modifiés. D’autres éléments sont présents et ne doivent pas être modifiés. L’ordre des éléments ci-dessous ne reflète pas l’ordre dans lequel ils doivent être présents dans le fichier.

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

Plusieurs `<RootPath>` éléments peuvent être présents (un pour chaque dossier de fichiers de données source). Image Server recherche les chemins d’accès racine dans l’ordre spécifié pour trouver un fichier source particulier.
