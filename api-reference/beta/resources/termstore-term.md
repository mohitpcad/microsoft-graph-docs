---
title: "term resource type"
description: "Defines a term entity in the termStore"
author: mpathak123
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: resourcePageType
---

# term resource type

Namespace: microsoft.graph.termStore

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **term** resource represents the term used in the [microsoft.graph.termStore.store].


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List children](../api/termstore-set-list-children.md)|[term](../resources/termstore-term.md) collection|Get the terms from the children navigation property.|
|[Create children](../api/termstore-set-post-children.md)|[term](../resources/termstore-term.md)|Create a new children object.|
|[Update children](../api/termstore-set-update-children.md)|[term](../resources/termstore-term.md)|Update the properties of a children object.|
|[Get children](../api/termstore-set-get-term.md)|[term](../resources/termstore-term.md)|Read the properties and relationships of a [term](../resources/term.md) object.|
|[Delete children](../api/termstore-set-delete-children.md)|None|Delete a [term](../resources/termstore-term.md) object.|
|[List terms](../api/term-list.md)|[term](../resources/termstore-term.md) collection|Get a list of the [term](../resources/term.md) objects and their properties.|
|[Create term](../api/termstore-term-create.md)|[term](../resources/termstore-term.md)|Create a new [term](../resources/termstore-term.md) object.|
|[Get term](../api/termstore-term-get.md)|[term](../resources/termstore-term.md)|Read the properties and relationships of a [term](../resources/termstore-term.md) object.|
|[Update term](../api/termstore-term-update.md)|[term](../resources/termstore-term.md)|Update the properties of a [term](../resources/termstore-term.md) object.|
|[Delete term](../api/termstore-term-delete.md)|None|Deletes a [term](../resources/termstore-term.md) object.|
|[List children](../api/termstore-term-list-children.md)|[term](../resources/termstore-term.md) collection|Get the terms from the children navigation property.|
|[Create children](../api/termstore-term-post-children.md)|[term](../resources/termstore-term.md)|Create a new children object.|
|[Get children](../api/termstore-term-get-term.md)|[term](../resources/termstore-term.md)|Read the properties and relationships of a [term](../resources/term.md) object.|
|[Update children](../api/termstore-term-update-children.md)|[term](../resources/termstore-term.md)|Update the properties of a children object.|
|[Delete children](../api/termstore-term-delete-children.md)|None|Delete a [term](../resources/termstore-term.md) object.|
|[List relations](../api/termstore-term-list-relations.md)|[relation](../resources/termstore-relation.md) collection|Get the relations from the relations navigation property.|
|[Create relations](../api/termstore-term-post-relations.md)|[relation](../resources/termstore-relation.md)|Create a new relations object.|
|[Get relations](../api/termstore-term-get-relation.md)|[relation](../resources/termstore-relation.md)|Read the properties and relationships of a [relation](../resources/relation.md) object.|
|[Update relations](../api/termstore-term-update-relations.md)|[relation](../resources/termstore-relation.md)|Update the properties of a relations object.|
|[Delete relations](../api/termstore-term-delete-relations.md)|None|Delete a [relation](../resources/termstore-relation.md) object.|
|[List set](../api/termstore-term-list-set.md)|[set](../resources/termstore-set.md) collection|Get the sets from the set navigation property.|
|[Add set](../api/termstore-term-post-set.md)|[set](../resources/termstore-set.md)|Add set by posting to the set collection.|
|[Remove set](../api/termstore-term-delete-set.md)|None|Remove a [set](../resources/termstore-set.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|Date and time of term creation. Read-only|
|descriptions|[localizedDescription](../resources/termstore-localizeddescription.md) collection|Description about term that is dependent on the languageTag|
|id|String|Unique identifier of term. Read-Only)|
|labels|[localizedLabel](../resources/termstore-localizedlabel.md) collection||Label meta-data for a term|
|lastModifiedDateTime|DateTimeOffset|Last date and time of term modification. Read-only|
|properties|[keyValue](../resources/termstore-intune-keyvalue.md) collection|Collection of properties on the term|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|children|[term](../resources/termstore-term.md) collection|Children of current term|
|relations|[relation](../resources/termstore-relation.md) collection|To indicate which terms are related to the current term as either pinned or reused|
|set|[set](../resources/termstore-set.md)|The set in which the term is created|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termStore.term",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termStore.term",
  "id": "String (identifier)",
  "labels": [
    {
      "@odata.type": "microsoft.graph.termStore.localizedLabel"
    }
  ],
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "descriptions": [
    {
      "@odata.type": "microsoft.graph.termStore.localizedDescription"
    }
  ],
  "properties": [
    {
      "@odata.type": "microsoft.graph.termStore.keyValue"
    }
  ]
  
  /*  relationships  */
  "children" : [{"@odata.type" : "microsoft.graph.termStore.term"}],
  "set" : {"@odata.type" : "microsoft.graph.termStore.set"}, 
  "relations" : [{"@odata.type" : "microsoft.graph.termStore.relation"}]
}
```

[microsoft.graph.termStore.localizedLabel]: termstore-localizedlabel.md
[microsoft.graph.termStore.term]: termstore-term.md
[microsoft.graph.termStore.set]: termstore-set.md
[microsoft.graph.termStore.relation]: termstore-relation.md
[microsoft.graph.termStore.localizedDescription]: termstore-localizeddescription.md
[microsoft.graph.termStore.store]: termstore-store.md

<!--
{
  "type": "#page.annotation",
  "description": "Term is the entity used for tagging in termStore",
  "keywords": "term,facet,resource",
  "section": "documentation",
  "tocPath": "Terms",
  "tocBookmarks": {
    "Resources/termstore-term": "#"
  },
  "suppressions": []
}
-->
