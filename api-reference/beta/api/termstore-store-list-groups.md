---
title: "List groups"
description: "Get the groups from the groups navigation property."
author: mohitpcad
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: apiPageType
---

# List groups
Namespace: microsoft.graph.termStore

Get the groups from the groups navigation property.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account) | Sites.Read.All and TermStore.Read.All, Sites.Read.All and TermStore.ReadWrite.All |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Not Supported. |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->

``` http
GET /termStore/groups
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [group](../resources/termstore-group.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_group"
}
-->

``` http
GET https://graph.microsoft.com/beta/termStore/groups
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "collection(microsoft.graph.termStore.group)"
} -->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "85825593-5593-8582-9355-828593558285",
      "createdDateTime": "2019-06-21T20:01:37Z",
      "description": "My term group",
      "scope" : "global",
      "displayName": "myGroup"  
    }
  ]
}
```

<!--
{
  "type": "#page.annotation",
  "description": "Get termGroup entity in termStore",
  "keywords": "term,termStore",
  "section": "documentation",
  "tocPath": "termStore/List termGroups",
  "suppressions": [
  ]
}
-->

