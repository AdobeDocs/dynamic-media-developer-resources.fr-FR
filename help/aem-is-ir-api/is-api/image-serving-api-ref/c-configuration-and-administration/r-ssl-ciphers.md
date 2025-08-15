---
description: La balise Connector du fichier server.xml prend en charge un attribut ciphers pour limiter les chiffrements pouvant être choisis pour une connexion SSL.
solution: Experience Manager
title: Définir des chiffrements SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Définir des chiffrements SSL{#defining-ssl-ciphers}

La balise Connector du fichier server.xml prend en charge un attribut ciphers pour limiter les chiffrements pouvant être choisis pour une connexion SSL.

Par défaut, tous les chiffrements sont disponibles. La liste est séparée par des virgules et peut contenir l’une des valeurs suivantes :

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

Si l’une des valeurs est incorrecte, Tomcat active chaque chiffrement. Il est donc essentiel de vérifier avec un outil externe après la configuration pour voir quels chiffrements sont réellement activés.

À titre d’exemple, la configuration suivante active uniquement les suites de chiffrement « 128 bits » et ultérieures :

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`
