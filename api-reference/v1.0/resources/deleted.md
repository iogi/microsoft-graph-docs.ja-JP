---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Deleted
ms.openlocfilehash: 1d45219b2ef26bdc96c46e386d66d91874f9bc0b
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2017
---
# <a name="deleted-facet"></a>Deleted ファセット

**Deleted** リソースは、アイテムが削除されたことを示します。
このバージョンの API では、リソースの値が存在する (null 以外である) ことは、ファイルが削除されたことを示します。
null (または存在しない) 値は、ファイルが削除されていないことを示します。

変更の追跡と削除済みアイテムの検出の詳細については、「[アイテムの変更を表示する](../api/driveitem_delta.md)」を参照してください。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  "state"
  ],
  "@odata.type": "microsoft.graph.deleted"
}-->
```json
{
  "state": "string"
}
```
## <a name="properties"></a>プロパティ

| プロパティ | 型   | 説明                               |
|:---------|:-------|:------------------------------------------|
| state    | String | 削除されたアイテムの状態を表します。 |

## <a name="remarks"></a>注釈 

DriveItem のファセットの詳細については、「[DriveItem](driveitem.md)」を参照してください。

<!-- {
  "type": "#page.annotation",
  "description": "The deleted facet providers properties about deleted items",
  "keywords": "deleted,delete,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Deleted"
} -->
