---
title: "set resource type"
description:  "Describes the termSet in the termStore"
author: mpathak123
ms.author: mopathak
localization_priority: Normal
ms.prod: "sharepoint-taxonomy"
doc_type: resourcePageType
---

# set resource type

Namespace: microsoft.graph.termStore

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

The **set** resource represents the set used in the [microsoft.graph.termStore.store].


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[List sets](../api/set-list.md)|[set](../resources/termstore-set.md) collection|Get a list of the [set](../resources/set.md) objects and their properties.|
|[Create set](../api/termstore-set-create.md)|[set](../resources/termstore-set.md)|Create a new [set](../resources/termstore-set.md) object.|
|[Get set](../api/termstore-set-get.md)|[set](../resources/termstore-set.md)|Read the properties and relationships of a [set](../resources/termstore-set.md) object.|
|[Update set](../api/termstore-set-update.md)|[set](../resources/termstore-set.md)|Update the properties of a [set](../resources/termstore-set.md) object.|
|[Delete set](../api/termstore-set-delete.md)|None|Deletes a [set](../resources/termstore-set.md) object.|
|[List children](../api/termstore-set-list-children.md)|[term](../resources/termstore-term.md) collection|Get the terms from the children navigation property.|
|[Create children](../api/termstore-set-post-children.md)|[term](../resources/termstore-term.md)|Create a new children object.|
|[Get children](../api/termstore-set-get-term.md)|[term](../resources/termstore-term.md)|Read the properties and relationships of a [term](../resources/term.md) object.|
|[Update children](../api/termstore-set-update-children.md)|[term](../resources/termstore-term.md)|Update the properties of a children object.|
|[Delete children](../api/termstore-set-delete-children.md)|None|Delete a [term](../resources/termstore-term.md) object.|
|[List parentGroup](../api/termstore-set-list-parentgroup.md)|[group](../resources/termstore-group.md) collection|Get the groups from the parentGroup navigation property.|
|[Create parentGroup](../api/termstore-set-post-parentgroup.md)|[group](../resources/termstore-group.md)|Create a new parentGroup object.|
|[Get parentGroup](../api/termstore-set-get-group.md)|[group](../resources/termstore-group.md)|Read the properties and relationships of a [group](../resources/group.md) object.|
|[Update parentGroup](../api/termstore-set-update-parentgroup.md)|[group](../resources/termstore-group.md)|Update the properties of a parentGroup object.|
|[Delete parentGroup](../api/termstore-set-delete-parentgroup.md)|None|Delete a [group](../resources/termstore-group.md) object.|
|[List relations](../api/termstore-set-list-relations.md)|[relation](../resources/termstore-relation.md) collection|Get the relations from the relations navigation property.|
|[Create relations](../api/termstore-set-post-relations.md)|[relation](../resources/termstore-relation.md)|Create a new relations object.|
|[Get relations](../api/termstore-set-get-relation.md)|[relation](../resources/termstore-relation.md)|Read the properties and relationships of a [relation](../resources/relation.md) object.|
|[Update relations](../api/termstore-set-update-relations.md)|[relation](../resources/termstore-relation.md)|Update the properties of a relations object.|
|[Delete relations](../api/termstore-set-delete-relations.md)|None|Delete a [relation](../resources/termstore-relation.md) object.|
|[List terms](../api/termstore-set-list-terms.md)|[term](../resources/termstore-term.md) collection|Get the terms from the terms navigation property.|
|[Create terms](../api/termstore-set-post-terms.md)|[term](../resources/termstore-term.md)|Create a new terms object.|
|[Get terms](../api/termstore-set-get-term.md)|[term](../resources/termstore-term.md)|Read the properties and relationships of a [term](../resources/term.md) object.|
|[Update terms](../api/termstore-set-update-terms.md)|[term](../resources/termstore-term.md)|Update the properties of a terms object.|
|[Delete terms](../api/termstore-set-delete-terms.md)|None|Delete a [term](../resources/termstore-term.md) object.|

## Properties
|Property|Type|Description|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|**Date and time of set creation. Read-only.**|
|description|String|**Description giving details on the term usage**|
|id|String|**Unique identifier of set. Read-only** Inherited from [entity](../resources/termstore-entity.md)|
|localizedNames|[localizedName](../resources/termstore-localizedname.md) collection|**Name of set for each languageTag**|
|properties|[keyValue](../resources/termstore-intune-keyvalue.md) collection|**Custom properties for set**|

## Relationships
|Relationship|Type|Description|
|:---|:---|:---|
|children|[term](../resources/termstore-term.md) collection|**Children terms of termSet**|
|parentGroup|[group](../resources/termstore-group.md)|**Group containing the particular set**|
|relations|[relation](../resources/termstore-relation.md) collection|**To indicate which terms have been pinned or reused directly under the termSet**|
|terms|[term](../resources/termstore-term.md) collection|**All the terms under the set**|

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.termStore.set",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.termStore.set",
  "id": "String (identifier)",
  "localizedNames": [
    {
      "@odata.type": "microsoft.graph.termStore.localizedName"
    }
  ],
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "properties": [
    {
      "@odata.type": "microsoft.graph.termStore.keyValue"
    }
  ]
  
  /*  relationships  */
  "children" : [{"@odata.type" : "microsoft.graph.termStore.term"}],
  "parentGroup" : {"odata.type" : "microsoft.graph.termStore.group"},
  "relations" : [{"@odata.type" : "microsoft.graph.termStore.relation"}] ,
  "terms" :  [{"@odata.type" : "microsoft.graph.termStore.term"}]
}
```

[microsoft.graph.termStore.term]: termstore-term.md
[microsoft.graph.termStore.set]: termstore-set.md
[microsoft.graph.termStore.group]: termstore-group.md
[microsoft.graph.termStore.relation]: termstore-relation.md
[microsoft.graph.termStore.store]: termstore-store.md
[microsoft.graph.termStore.localizedName]: termstore-localizedname.md

<!--
{
  "type": "#page.annotation",
  "description": "TermSet is the entity containing the particular taxonomy for a tenant",
  "keywords": "termSet,facet,resource",
  "section": "documentation",
  "tocPath": "TermSet",
  "tocBookmarks": {
    "Resources/termStore.set": "#"
  },
  "suppressions": []
}
-->
