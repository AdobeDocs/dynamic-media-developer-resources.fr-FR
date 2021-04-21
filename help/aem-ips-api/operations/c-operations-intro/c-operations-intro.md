---
description: Décrit les paramètres d'opération courants gérés par l'API Service Web IPS.
solution: Experience Manager
title: Méthodes d'exploitation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---


# Méthodes d&#39;exploitation{#operations-methods}

Cette section décrit les paramètres d&#39;opération courants gérés par l&#39;API Service Web IPS.

Pour une description complète de chaque paramètre d&#39;opération, voir [Paramètres d&#39;opération](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles : À propos de {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gère les objets IPS de référence renvoyés par certaines opérations d&#39;API. Vous pouvez également transmettre des poignées en tant que paramètres aux appels d’opération suivants. Les gestionnaires sont des types de données de chaîne ( `xsd:string`).

Les poignées sont destinées à être utilisées pendant une seule session d’application uniquement. En outre, vous devez rendre les poignées persistantes car leur format peut changer d&#39;une version d&#39;IPS à l&#39;autre. Lorsque vous créez des applications interactives, vous mettez en oeuvre des délais d&#39;expiration de session et ignorez toutes les poignées entre les sessions, en particulier après une mise à niveau d&#39;IPS. Lorsque vous écrivez des applications non interactives, appelez les opérations appropriées pour récupérer les poignées chaque fois que l’application est exécutée. Les exemples de code Java/Axis2 suivants montrent une exécution de code incorrecte et correcte :

**Code de poignée incorrect**

Cet exemple de code est incorrect, car il contient une valeur codée en dur (555) pour la poignée de société.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Corriger le code de poignée**

Cet exemple de code est correct car il appelle `getCompanyInfo` pour renvoyer un handle valide. Elle ne repose pas sur une valeur codée en dur. Utilisez cette méthode ou tout autre équivalent d&#39;API IPS pour renvoyer la poignée requise.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Types de poignée courants {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

Pour la plupart des opérations, vous devez définir un contexte de société en transmettant un paramètre `companyHandle`. La poignée de société est un pointeur renvoyé par certaines opérations telles que `getCompanyInfo`, `addCompany` et `getCompanyMembership`.

**userHandle**

Le paramètre `userHandle` est un paramètre facultatif pour les opérations qui cible un utilisateur spécifique. Par défaut, ces opérations cible l’utilisateur appelant (l’utilisateur dont les informations d’identification sont transmises pour authentification). Cependant, les administrateurs disposant des autorisations appropriées peuvent spécifier un autre utilisateur. Par exemple, l&#39;opération `setPassword` définit normalement le mot de passe de l&#39;utilisateur authentifié, mais un administrateur peut utiliser le paramètre `userHandle` pour définir le mot de passe d&#39;un autre utilisateur.

Pour les opérations nécessitant un contexte de société (à l&#39;aide du paramètre `companyHandle`), les utilisateurs authentifiés et les utilisateurs de cible doivent être membres de la société spécifiée. Pour les opérations qui ne nécessitent pas de contexte de société, les utilisateurs authentifiés et les utilisateurs de cible doivent tous deux être membres d’au moins une société commune.

Les opérations suivantes permettent de récupérer les poignées d’utilisateur :

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle et accessGroupHandle**

Par défaut, les opérations qui nécessitent des autorisations d’accès (lecture, écriture, suppression) fonctionnent dans le contexte des autorisations de l’utilisateur appelant. Certaines opérations vous permettent de modifier ce contexte avec le paramètre `accessUserHandle` ou `accessGroupHandle`. Le paramètre `accessUserHandle` permet à un administrateur d&#39;emprunter l&#39;identité d&#39;un autre utilisateur. Le paramètre `accessGroupHandle` permet à l&#39;appelant de fonctionner dans le contexte d&#39;un groupe d&#39;utilisateurs spécifique.

**responseFieldArray et excludeFieldArray**

Certaines opérations permettent à l’appelant de limiter les champs inclus dans la réponse. Le fait de limiter les champs permet de réduire le temps et la mémoire nécessaires au traitement de la demande et de réduire la taille des données de réponse. L&#39;appelant peut demander une liste spécifique de champs en transmettant un paramètre `responseFieldArray` ou avec une liste énumérée de champs exclus via le paramètre `excludeFieldArray`.

`responseFieldArray` et `excludeFieldArray` spécifient des champs en utilisant un chemin de noeud séparé par `/`. Par exemple, pour indiquer que `searchAssets` renvoie uniquement le nom, la date de dernière modification et les métadonnées de chaque fichier, faites référence aux éléments suivants :

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

Notez que les chemins d’accès aux noeuds sont relatifs à la racine de noeud renvoyée. Si vous spécifiez un champ de type complexe sans aucun de ses sous-éléments (par exemple, `assetArray/items/imageInfo`), tous ses sous-éléments sont inclus. Si vous spécifiez un ou plusieurs sous-éléments dans un champ de type complexe (par exemple, `assetArray/items/imageInfo/originalPath`), seuls ces sous-éléments sont inclus.

Si vous n’incluez pas `responseFieldArray` ou `excludeFieldArray` dans une requête, tous les champs sont renvoyés.

**Paramètres régionaux**

Depuis IPS 4.0, l&#39;API IPS prend en charge la définition du contexte régional d&#39;une opération en transmettant le paramètre régional `authHeader`. Si le paramètre régional n’est pas présent, l’en-tête HTTP `Accept-Language` est utilisé. Si cet en-tête n&#39;est pas non plus présent, les paramètres régionaux par défaut du serveur IPS sont utilisés.

Certaines opérations utilisent également des paramètres régionaux explicites, qui peuvent être différents du contexte régional de l’opération. Par exemple, l’opération `submitJob` utilise un paramètre `locale` qui définit les paramètres régionaux utilisés pour la journalisation des tâches et la notification par courrier électronique.

Les paramètres régionaux utilisent le format `<language_code>[-<country_code>]`

Lorsque le code de langue est un code en minuscules à deux lettres spécifié par ISO-639 et que le code de pays facultatif est un code en majuscules à deux lettres spécifié par ISO-3266. Par exemple, la chaîne de paramètres régionaux pour l’anglais américain est `en-US`.
