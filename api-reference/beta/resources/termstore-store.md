---
title: "store resource type"
description:  "Describes the top-level store in the termStore"
author: mpathak123
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: "resourcePageType"
---

# store resource type

Namespace: microsoft.graph.termStore

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **store** resource represents the term-store for taxonomy.


Inherits from [entity](../resources/entity.md).

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termStore.store",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termStore.store",
  "id": "String (identifier)",
  "defaultLanguageTag": "String",
  "languageTags": [
    "String"
  ],
  /*  relationships  */
  "groups" : [{"@odata.type" : "microsoft.graph.termStore.group"}] ,
  "sets" : [{"oData.type" : "microsoft.graph.termStore.set"}]
}
```

