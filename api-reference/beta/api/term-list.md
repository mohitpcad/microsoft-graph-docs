---
title: "List terms"
description: "Get a list of the term objects and their properties."
author: mpathak123
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: apiPageType
---

# List terms
Namespace: microsoft.graph.termStore

Get a list of the [term](../resources/term.md) objects and their properties.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/concepts/permissions-reference.md).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated| TermStore.Read.All, TermStore.ReadWrite.All |

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /termStore/groups/{groupId}/sets/{setId}/children
GET /termStore/groups/{groupId}/sets/{setId}/terms/{termId}/children
GET /termStore/sets/{setId}/children
GET /termStore/sets/{setId}/terms/{termId}/children
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Response

If successful, this method returns a `200 OK` response code and a collection of [term](../resources/term.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_term"
}
-->
``` http
GET https://graph.microsoft.com/beta/termStore/groups/{groupId}/sets/{setId}/children
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "collection(microsoft.graph.termstore.term)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json
{
  "value": [
    {
  "createdDateTime": "2019-06-21T20:01:37Z",
  "id": "1FFD3F87-9464-488A-A0EC-8FB90911182C",
  "labels" : [
      {
          "name" : "Car",
          "languageTag" : "en-US",
          "isDefault" : true
      }
  ],
  "lastModifiedDateTime": "2019-06-21T20:01:37Z"
},
{
  "createdDateTime": "2019-09-21T20:41:37Z",
  "id": "3CEB0050-69A1-40E7-A427-83E2FAC80C27",
  "labels" : [
      {
          "name" : "bike",
          "languageTag" : "en-US",
          "isDefault" : true
      }
  ],
  "lastModifiedDateTime": "2019-11-21T23:41:37Z"
}
]
}
```
[microsoft.graph.termStore.term]: ../resources/termstore-term.md
[microsoft.graph.termStore.set]: ../resources/termstore-set.md

<!--
{
  "type": "#page.annotation",
  "description": "Get children of a term or termSet in termStore",
  "keywords": "term,termStore",
  "section": "documentation",
  "tocPath": "termStore/Get termchildren",
  "suppressions": [
  ]
}
