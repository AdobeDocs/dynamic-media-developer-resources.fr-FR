---
title: Configuration requise et conditions préalables
description: Avant d’utiliser la diffusion d’images Dynamic Media, assurez-vous que votre système est conforme à la configuration requise.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
TQID: 'https://experienceleague.adobe.com/SKAe9OsVsSkTRR5E3s5lBcPct4CgG1h1uIh7ayIpINA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 390
ht-degree: 0%

---

# Configuration requise et conditions préalables{#system-requirements-and-prerequisites}

Avant d’utiliser la diffusion d’images Dynamic Media, assurez-vous que votre système est conforme à la configuration requise.

## Matériel du serveur {#section-f3c14a7bc1b745118602659628df779f}

Votre serveur doit répondre aux exigences matérielles suivantes.

>[!NOTE]
>
>Les systèmes dotés de processeurs AMD64 et Intel® EM64T sont généralement configurés en tant que plateformes NUMA (Non Uniform Memory Architecture). Cela signifie que le noyau construit plusieurs nœuds de mémoire au moment du démarrage plutôt que de construire un seul nœud de mémoire. La construction de plusieurs nœuds peut entraîner un épuisement de la mémoire sur un ou plusieurs nœuds avant que d’autres nœuds ne s’épuisent. Lorsque l’épuisement de la mémoire se produit, le noyau peut décider d’interrompre les processus (par exemple, le serveur d’images ou le [!DNL Platform Server]) même s’il existe de la mémoire disponible. Par conséquent, Adobe recommande de désactiver NUMA si vous exécutez un tel système. Utilisez l’option de démarrage `numa=off` pour éviter que le noyau n’arrête ces processus.

**Windows**

* Intel Xeon® ou AMD® Opteron CPU avec au moins quatre cœurs.
* 1 Go de RAM minimum.
* L&#39;espace de permutation est égal à au moins deux fois la quantité de mémoire physique (RAM).
* 2 Go d’espace disque disponible pour l’installation et le fonctionnement de base, un espace disque supplémentaire est requis pour les images sources, les journaux, les caches de données et les fichiers de manifeste.
* Carte d&#39;interface réseau Fast Ethernet.

**Linux®**

* Intel Xeon® ou AMD® Opteron CPU avec au moins quatre cœurs.
* 16 Go de RAM minimum.
* Permutation désactivée (recommandé).
* 2 Go d’espace disque disponible pour l’installation et le fonctionnement de base, un espace disque supplémentaire est requis pour les images sources, les journaux, les caches de données et les fichiers de manifeste.
* Carte d&#39;interface réseau Fast Ethernet.

**Remarque (Linux®) : la diffusion d’images** ne fonctionne pas lorsque SELinux est activé. Cette option est activée par défaut. Pour désactiver SELinux, modifiez le fichier [!DNL /etc/selinux/config] et modifiez la valeur SELinux à partir de :

`SELINUX=enforcing`

Vers

`SELINUX=disabled`

**Remarque (Linux®) :** Assurez-vous que le nom d’hôte du serveur peut être résolu sur une adresse IP. Si cela s’avère impossible, ajoutez le nom d’hôte complet et l’adresse IP à [!DNL /etc/hosts], comme dans l’exemple suivant.

`<ip address> <fully qualified hostname>`

## Logiciel du serveur {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

La diffusion d’images Dynamic Media nécessite les logiciels de serveur suivants.

**Windows**

* ® Windows Server 2008.
* Système d’exploitation 64 bits.

**Linux®**

* Red Hat® Enterprise 5 ou CentOS 5.5 et versions ultérieures, avec les derniers correctifs.
* Système d’exploitation 64 bits.

**Remarque :** pour utiliser la diffusion d’images sous Windows, vous devez installer Microsoft® Visual Studio 2010.
