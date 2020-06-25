---
title: "relation resource type"
description: "Describes the entity for relations between terms in the termStore"
author: mpathak123
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: resourcePageType
---

# relation resource type

Namespace: microsoft.graph.termStore

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **microsoft.graph.termStore.relation** resource represents the relations between [microsoft.graph.termStore.term]. Currently two types of relations are supported between terms, the types are“pin” and “reuse” . In a “pin” relationship a term(“A”) can be pinned under a different term in a different termSet. In a pinned relationship new children to the term(“A”) can only be added in termSet in which term(“A”) was created. In terms of the UI any change in the hierarchy under term(“A”) gets reflected across termSets in which term(“A”) was pinned. The reused relationship is similar to the pinned except that changes to the reused term can be made from any hierarchy in which the term gets reused. Also in terms of UI changes in hierarchy made to the reused term do not get reflected in the other termSets where the term gets reused.

Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List relations](../api/termstore-set-list-relations.md)|[relation](../resources/termstore-relation.md) collection|Get the relations from the relations navigation property.|
|[Create relations](../api/termstore-set-post-relations.md)|[relation](../resources/termstore-relation.md)|Create a new relations object.|
|[Update relations](../api/termstore-set-update-relations.md)|[relation](../resources/termstore-relation.md)|Update the properties of a relations object.|
|[Get relations](../api/termstore-set-get-relation.md)|[relation](../resources/termstore-relation.md)|Read the properties and relationships of a [relation](../resources/relation.md) object.|
|[Delete relations](../api/termstore-set-delete-relations.md)|None|Delete a [relation](../resources/termstore-relation.md) object.|
|[List relations](../api/relation-list.md)|[relation](../resources/termstore-relation.md) collection|Get a list of the [relation](../resources/relation.md) objects and their properties.|
|[Create relation](../api/termstore-relation-create.md)|[relation](../resources/termstore-relation.md)|Create a new [relation](../resources/termstore-relation.md) object.|
|[Get relation](../api/termstore-relation-get.md)|[relation](../resources/termstore-relation.md)|Read the properties and relationships of a [relation](../resources/termstore-relation.md) object.|
|[Update relation](../api/termstore-relation-update.md)|[relation](../resources/termstore-relation.md)|Update the properties of a [relation](../resources/termstore-relation.md) object.|
|[Delete relation](../api/termstore-relation-delete.md)|None|Deletes a [relation](../resources/termstore-relation.md) object.|
|[List fromTerm](../api/termstore-relation-list-fromterm.md)|[term](../resources/termstore-term.md) collection|Get the terms from the fromTerm navigation property.|
|[Add fromTerm](../api/termstore-relation-post-fromterm.md)|[term](../resources/termstore-term.md)|Add fromTerm by posting to the fromTerm collection.|
|[Remove fromTerm](../api/termstore-relation-delete-fromterm.md)|None|Remove a [term](../resources/termstore-term.md) object.|
|[List set](../api/termstore-relation-list-set.md)|[set](../resources/termstore-set.md) collection|Get the sets from the set navigation property.|
|[Add set](../api/termstore-relation-post-set.md)|[set](../resources/termstore-set.md)|Add set by posting to the set collection.|
|[Remove set](../api/termstore-relation-delete-set.md)|None|Remove a [set](../resources/termstore-set.md) object.|
|[List toTerm](../api/termstore-relation-list-toterm.md)|[term](../resources/termstore-term.md) collection|Get the terms from the toTerm navigation property.|
|[Add toTerm](../api/termstore-relation-post-toterm.md)|[term](../resources/termstore-term.md)|Add toTerm by posting to the toTerm collection.|
|[Remove toTerm](../api/termstore-relation-delete-toterm.md)|None|Remove a [term](../resources/termstore-term.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|id|String|**TODO: Add Description** Inherited from [entity](../resources/termstore-entity.md)|
|relationship|relationType|**TODO: Add Description**. Possible values are: `pin`, `reuse`.|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|fromTerm|[term](../resources/termstore-term.md)|**TODO: Add Description**|
|set|[set](../resources/termstore-set.md)|**TODO: Add Description**|
|toTerm|[term](../resources/termstore-term.md)|**TODO: Add Description**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termStore.relation",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termStore.relation",
  "id": "String (identifier)",
  "relationship": "String"
  
  /*  relationships */
  "fromTerm" : { "@odata.type" : "microsoft.graph.termStore.term"},
  "toTerm" : { "@odata.type" : "microsoft.graph.termStore.term"},
  "set" : { "@odata.type" : "microsoft.graph.termStore.set"}
}
```

[microsoft.graph.termStore.term]: term.md
[microsoft.graph.termStore.set]: termSet.md
[microsoft.graph.termStore.relations]: termRelation.md
[microsoft.graph.termStore.relation]: termRelation.md

<!--
{
  "type": "#page.annotation",
  "description": "TermRelation is the entity for mapping relations between different terms",
  "keywords": "termRelation,facet,resource",
  "section": "documentation",
  "tocPath": "TermRelation",
  "tocBookmarks": {
    "Resources/termStore.relation": "#"
  },
  "suppressions": []
}
-->
