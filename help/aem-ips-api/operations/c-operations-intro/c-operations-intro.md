---
description: Décrit les paramètres d’opération courants gérés par l’API de service web IPS.
solution: Experience Manager
title: Méthodes d’exploitation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
TQID: 'https://experienceleague.adobe.com/ZoT9qmMjkkdVARrEvxhRn3Tvme1anUZ4-i1xLv0acb8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 717
ht-degree: 0%

---

# Méthodes d’exploitation{#operations-methods}

Cette section décrit les paramètres d’opération courants gérés par l’API de service web IPS.

Pour obtenir une description complète de chaque paramètre d&#39;opération, voir [Paramètres d&#39;opération](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles : À Propos {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gère les objets IPS de référence renvoyés par certaines opérations de l’API. Vous pouvez également transmettre des handles en tant que paramètres aux appels d’opération suivants. Les handles sont des types de données de chaîne ( `xsd:string`).

Les descripteurs sont destinés à être utilisés au cours d’une seule session d’application uniquement. En outre, vous devez rendre les handles persistants, car leur format peut changer entre les versions IPS. Lorsque vous écrivez des applications interactives, vous implémentez des délais d&#39;expiration de session et ignorez tous les descripteurs entre les sessions, en particulier après une mise à niveau IPS. Lorsque vous écrivez des applications non interactives, appelez les opérations appropriées pour récupérer les descripteurs à chaque exécution de l&#39;application. Les exemples de code Java/Axis2 suivants montrent une exécution de code incorrecte :

**Code de poignée incorrect**

Cet exemple de code est incorrect, car il contient une valeur codée en dur (555) pour le handle de l’entreprise.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Code de poignée correct**

Cet exemple de code est correct, car il appelle `getCompanyInfo` pour renvoyer un handle valide. Il ne repose pas sur une valeur codée en dur. Utilisez cette méthode, ou un autre équivalent de l’API IPS, pour renvoyer le handle requis.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Types de poignées communs {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

La plupart des opérations nécessitent de définir un contexte d’entreprise en transmettant un paramètre `companyHandle`. Le handle de l’entreprise est un pointeur renvoyé par certaines opérations telles que `getCompanyInfo`, `addCompany` et `getCompanyMembership`.

**userHandle**

Le paramètre `userHandle` est un paramètre facultatif pour les opérations qui ciblent un utilisateur spécifique. Par défaut, ces opérations ciblent l’utilisateur appelant (l’utilisateur dont les informations d’identification sont transmises pour l’authentification). Cependant, les utilisateurs administrateurs disposant des autorisations appropriées peuvent spécifier un autre utilisateur. Par exemple, l’opération `setPassword` définit normalement le mot de passe de l’utilisateur authentifié, mais un administrateur peut utiliser le paramètre `userHandle` pour définir le mot de passe d’un autre utilisateur.

Pour les opérations qui nécessitent un contexte de société (à l’aide du paramètre `companyHandle` ), les utilisateurs authentifiés et cibles doivent être membres de la société spécifiée. Pour les opérations qui ne nécessitent pas de contexte d’entreprise, les utilisateurs authentifiés et cibles doivent tous deux être membres d’au moins une société commune.

Les opérations suivantes peuvent récupérer les handles d’utilisateur :

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle et accessGroupHandle**

Par défaut, les opérations qui nécessitent des autorisations d’accès (lecture, écriture, suppression) s’effectuent dans le contexte d’autorisation de l’utilisateur appelant. Certaines opérations permettent de modifier ce contexte avec le paramètre `accessUserHandle` ou `accessGroupHandle` . Le paramètre `accessUserHandle` permet à un administrateur d’emprunter l’identité d’un autre utilisateur. Le paramètre `accessGroupHandle` permet à l’appelant d’agir dans le contexte d’un groupe d’utilisateurs spécifique.

**responseFieldArray et excludeFieldArray**

Certaines opérations permettent à l’appelant de restreindre les champs inclus dans la réponse. La limitation des champs peut contribuer à réduire le temps et la mémoire nécessaires au traitement de la requête ainsi que la taille des données de réponse. L’appelant peut demander une liste spécifique de champs en transmettant un paramètre de `responseFieldArray` ou avec une liste énumérée de champs exclus au moyen du paramètre de `excludeFieldArray`.

`responseFieldArray` et `excludeFieldArray` spécifient des champs à l’aide d’un chemin de nœud séparé par des `/`. Par exemple, pour indiquer que `searchAssets` renvoie uniquement le nom, la date de dernière modification et les métadonnées de chaque ressource, reportez-vous aux éléments suivants :

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

De même, pour renvoyer tous les champs (à l’exception des autorisations) :

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Notez que les chemins d’accès aux nœuds sont relatifs à la racine de nœud renvoyée. Si vous spécifiez un champ de type complexe sans aucun de ses sous-éléments (par exemple, `assetArray/items/imageInfo`), tous ses sous-éléments sont inclus. Si vous spécifiez un ou plusieurs sous-éléments dans un champ de type complexe (par exemple, `assetArray/items/imageInfo/originalPath`), seuls ces sous-éléments sont inclus.

Si vous n’incluez pas de `responseFieldArray` ou de `excludeFieldArray` dans une requête, tous les champs sont renvoyés.

**Paramètres régionaux**

Depuis IPS 4.0, l’API IPS prend en charge la définition du contexte des paramètres régionaux d’une opération en transmettant le paramètre régional `authHeader`. Si le paramètre régional n’est pas présent, le `Accept-Language` d’en-tête HTTP est utilisé. Si cet en-tête n’est pas non plus présent, le paramètre régional par défaut du serveur IPS est utilisé.

Certaines opérations utilisent également des paramètres régionaux explicites, qui peuvent être différents du contexte des paramètres régionaux de l’opération. Par exemple, l’opération `submitJob` prend un paramètre de `locale` qui définit les paramètres régionaux utilisés pour la journalisation des tâches et les notifications par e-mail.

Les paramètres régionaux utilisent le format `<language_code>[-<country_code>]`

Lorsque le code langue est un code à deux lettres en minuscules spécifié par la norme ISO-639 et le code pays facultatif est un code à deux lettres en majuscules spécifié par la norme ISO-3266. Par exemple, la chaîne du paramètre régional pour l’anglais américain est `en-US`.

