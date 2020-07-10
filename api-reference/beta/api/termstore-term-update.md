---
title: "Update term"
description: "Update the properties of a term object."
author: mohitpcad
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: apiPageType
---

# Update term
Namespace: microsoft.graph.termStore

Update the properties of a [term](../resources/termstore-term.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from most to least privileged)|
|:---|:---|
|Delegated (work or school account) | Sites.Read.All and TermStore.ReadWrite.All |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Not supported |


## HTTP request

<!-- {
  "blockType": "ignored"
}-->

``` http
PATCH /termStore/sets/{setId}/terms/{termId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [term](../resources/termstore-term.md) object.

The following table shows the properties that can be updated for a [term](../resources/termstore-term.md).

|Property|Type|Description|
|:---|:---|:---|
|labels|[localizedLabel](../resources/termstore-localizedlabel.md) collection|labels of a term|
|descriptions|[localizedDescription](../resources/termstore-localizeddescription.md) collection|description about the term|
|properties|[keyValue](../resources/keyvalue.md) collection|properties associated with the term|



## Response

If successful, this method returns a `200 OK` response code and an updated [term](../resources/termstore-term.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_term"
} -->

``` http
PATCH https://graph.microsoft.com/beta/termStore/sets/{setId}/terms/{termId}
Content-Type: application/json
Content-length: 366

{
  "labels" : [
      {
          "name" : "changedLabel",
          "languageTag" : "en-US",
          "isDefault" : true
      }
  ]
}
```


### Response
**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.termStore.term"
}-->

``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "id": "81be9856-9856-81be-5698-be815698be81",
  "labels" : [
      {
          "name" : "changedLabel",
          "languageTag" : "en-US",
          "isDefault" : true
      }
  ]
}
```

[microsoft.graph.termStore.term]: ../resources/termstore-term.md

<!--
{
  "type": "#page.annotation",
  "description": "Get term entity in termStore",
  "keywords": "term,termStore",
  "section": "documentation",
  "tocPath": "termStore/Update term",
  "suppressions": [
  ]
}
-->
