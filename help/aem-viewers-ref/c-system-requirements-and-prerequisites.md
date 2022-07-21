---
title: Configuration requise pour les visionneuses Dynamic Media HTML5
description: Configuration requise pour les visionneuses Dynamic Media HTML5.
solution: Experience Manager
contentOwner: Rick Brough
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: e4543358-92a6-4acc-a8a2-227e1daea722
source-git-commit: 8e09f8168987788f7d55849b4a275c488cfcc0b9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 2%

---

# Configuration requise des visionneuses Dynamic Media HTML5{#system-requirements}

Configuration requise pour les visionneuses Dynamic Media HTML5.

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Matériel et logiciels du serveur {#section-05099146f1f0418988c196635110bee6}

<!-- Updated March 03, 2022 Contact is now Deepa Gupta -->

* Adobe Dynamic Media Image Serving 6.7.1 ou version ultérieure.
* Les visionneuses HTML5 requièrent des bibliothèques SDK JavaScript côté serveur 3.11.5 ou version ultérieure.
* *Envoyer un courrier électronique à un ami* les fonctions sociales requièrent s7ondemand 5.0.9 ou version ultérieure.
* Visionneuse de catalogue électronique - [Fenêtre contextuelle du panneau Infos](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/r-html5-ecatalog-viewer-20-customize-infopanelpopup.md) La prise en charge nécessite info server 2.1.8 ou version ultérieure.
* Les composants des fonctionnalités de recherche requièrent s7search 2.3.0 ou version ultérieure.

## Configuration requise des visionneuses {#section-cc72b1e209524d038b4d5b92b35e998e}

**Configuration requise du navigateur client pour les visionneuses de composants :**

* Pris en charge sur les versions de système d’exploitation suivantes ou ultérieures :
   * Microsoft® Windows® 7
   * macOS X 10.12
* Pris en charge sur les versions de navigateur/plateforme suivantes ou ultérieures :
   * Android™ OS 4.x
   * BlackBerry® 10 sur les navigateurs natifs. Seule la lecture vidéo est prise en charge.
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS6
   * iPad 2 (navigateurs Safari et Chrome uniquement)
   * iPhone 3GS
   * Safari 11
* Internet Explorer sur les périphériques mobiles n’est pas pris en charge.
* *PanoramicViewer* est pris en charge sur les versions de navigateur/plateforme suivantes ou ultérieures :
   * Android™ 4.4 (appareils mobiles uniquement)
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11
* *Visionneuse de vidéos 360x* et *DimensionalViewer* est pris en charge sur les versions de navigateur/plateforme suivantes ou ultérieures :
   * Android™ 5 (appareils mobiles uniquement)
   * Chrome 82
   * Edge
   * Firefox 77
   * iOS 12
   * Safari 12
* *ZoomVerticalViewer* est pris en charge sur les versions de navigateur/plateforme suivantes ou ultérieures :
   * Android™ 4.x
   * Chrome 82
   * Edge
   * Firefox 77
   * Internet Explorer 11
   * iOS 10
   * Safari 11

**IMPORTANT**
À compter du 30 septembre 2022, les visionneuses Dynamic Media Adobe ne prendront plus en charge les éléments suivants :

* TLS (Transport Layer Security) 1.0 et 1.1
* Les chiffrements faibles suivants dans TLS 1.2 :
   * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA384`
   * `TLS_ECDHE_RSA_WITH_AES_256_CBC_SHA`
   * `TLS_RSA_WITH_AES_256_GCM_SHA384`
   * `TLS_RSA_WITH_AES_256_CBC_SHA256`
   * `TLS_RSA_WITH_AES_256_CBC_SHA`
   * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA256`
   * `TLS_ECDHE_RSA_WITH_AES_128_CBC_SHA`
   * `TLS_RSA_WITH_AES_128_GCM_SHA256`
   * `TLS_RSA_WITH_AES_128_CBC_SHA256`
   * `TLS_RSA_WITH_AES_128_CBC_SHA`
   * `TLS_RSA_WITH_CAMELLIA_256_CBC_SHA`
   * `TLS_RSA_WITH_CAMELLIA_128_CBC_SHA`
   * `TLS_ECDHE_RSA_WITH_3DES_EDE_CBC_SHA`
   * `TLS_RSA_WITH_SDES_EDE_CBC_SHA`

<!-- Effective September 30, 2018, Adobe Dynamic Media Classic Viewers ended support of Transport Layer Security 1.0 (TLS 1.0). As such, Dynamic Media Classic no longer supports viewers on the following browsers/platforms that support TLS 1.0 (Adobe recommends using TLS 1.2 or later):

* Android™ 2.3.7
* Android™ 4.0.4
* Android™ 4.1.1
* Android™ 4.2.2
* Android™ 4.3
* Internet Explorer 7 on Window Vista®
* Internet Explorer 8 on Windows® XP
* Internet Explorer 8-10 on Windows® 7
* Internet Explorer 10 on Windows® Phone 8.0
* Safari 5.1.9 on Apple OS X 10.6.8
* Safari 6.0.4 on Apple OS X 10.8.4
* Java™ 6u45
* Java™ 7u25
* OpenSSL 0.9.8y
* Baidu January 2015 -->

<!-- FLASH VIEWERS END-OF-LIFE — Effective January 31, 2017, Adobe Dynamic Media Classic officially ended support for the Flash viewer platform. -->
