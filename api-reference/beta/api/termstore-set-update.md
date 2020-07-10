---
title: "Update set"
description: "Update the properties of a set object."
author: mohitpcad
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: apiPageType
---

# Update set
Namespace: microsoft.graph.termStore

Update the properties of a [set](../resources/termstore-set.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account) |Sites.Read.All and TermStore.ReadWrite.All |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Not supported |


## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

``` http
PATCH /termStore/sets/{setId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [set](../resources/termstore-set.md) object.

The following table shows the properties that can be edited for the [set](../resources/termstore-set.md).

|Property|Type|Description|
|:---|:---|:---|
|localizedNames|[localizedName](../resources/termstore-localizedname.md) collection|Name of the set|
|description|String|Description of the set|
|properties|[keyValue](../resources/keyvalue.md) collection|properties of a set|



## Response

If successful, this method returns a `200 OK` response code and an updated [set](../resources/termstore-set.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_set"
} -->

``` http
PATCH https://graph.microsoft.com/beta/termStore/sets/{setId}
Content-Type: application/json
Content-length: 288

{
  "description": "mySet"
}
```


### Response

**Note:** The response object shown here might be shortened for readability.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.termStore.set"
}-->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "3607e9f9-e9f9-3607-f9e9-0736f9e90736",
  "description": "mySet",    
  "localizedNames" : [
    {
      "languageTag" : "en-US",
      "name" : "Department"
    }
  ]
}
```

<!--
{
  "type": "#page.annotation",
  "description": "Get termSet entity in termStore",
  "keywords": "term,termStore",
  "section": "documentation",
  "tocPath": "termStore/Update termSet",
  "suppressions": [
  ]
}
-->
