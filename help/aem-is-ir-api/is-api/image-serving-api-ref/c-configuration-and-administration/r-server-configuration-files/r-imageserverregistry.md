---
description: Contient les paramètres de configuration du serveur d’images.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
TQID: 'https://experienceleague.adobe.com/UdMACutToNmpsXnhU0jAaItCZJ8r0RTxirjaqXSpa0c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Contient les paramètres de configuration du serveur d’images.

Lors de la modification de ce fichier XML, veillez à conserver une syntaxe XML valide, sinon le serveur d’images risque de ne pas démarrer.

Pour que les modifications soient prises en compte, redémarrez le serveur d’images après avoir modifié ce fichier. Seules les valeurs d’élément répertoriées ci-dessous sont prises en charge pour la modification. Modifiez tout autre contenu de ce fichier uniquement sur avis du support technique de Dynamic Media.

>[!NOTE]
>
>Ne modifiez pas la structure des `<imageserverregistry>`, y compris l’ordre des éléments. Soyez prudent lorsque vous modifiez ce fichier, sinon le serveur d’images risque de ne pas démarrer.

Les éléments suivants illustrent ceux qui peuvent être modifiés. D’autres éléments sont présents et ne doivent pas être modifiés. L’ordre des éléments ci-dessous ne reflète pas l’ordre dans lequel ils doivent être présents dans le fichier.

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

Plusieurs éléments de `<RootPath>` peuvent être présents (un pour chaque dossier de fichiers de données sources). Le serveur d’images recherche les chemins d’accès racine dans l’ordre spécifié pour trouver un fichier source particulier.
