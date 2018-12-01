---
title: directory リソースの種類 (削除済みアイテム)
description: . 削除されたアイテムは、最大 30 日間、復元可能な状態に維持されます。 30 日が経過すると、アイテムは完全に削除されます。
ms.openlocfilehash: 74b4d1ff94b567557fd90701b1c4bae479a8317e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27073673"
---
# <a name="directory-resource-type-deleted-items"></a>directory リソースの種類 (削除済みアイテム)

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

ディレクトリ内の削除済みアイテムを表します。 アイテムが削除されると、そのアイテムは削除済みアイテムの「コンテナー」に追加されます。 削除されたアイテムは、最大 30 日間、復元可能な状態に維持されます。 30 日が経過すると、アイテムは完全に削除されます。

現在、[削除済みアイテム] 機能は Office 365 の [group](group.md) および [user](users.md) リソースに対してのみサポートされています。

## <a name="methods"></a>メソッド

| メソッド         | 戻り値の型 | 説明 |
|:---------------|:------------|:------------|
|[削除済みアイテムの取得](../api/directory-deleteditems-get.md) | [directoryObject](directoryobject.md) | 削除済みアイテムのプロパティを取得します。 |
|[削除済みアイテムの復元](../api/directory-deleteditems-restore.md) |[directoryObject](directoryobject.md)| 最近削除されたアイテムを復元します。 |
|[削除済みアイテムの一覧表示](../api/directory-deleteditems-list.md) |[directoryObject](directoryobject.md) コレクション| 最近削除されたアイテムのリストを取得します。 |
|[アイテムの完全削除](../api/directory-deleteditems-delete.md) | なし | アイテムを完全に削除します。 |
|[ユーザーによって所有されている削除済みのアイテムを一覧表示します。](../api/directory-deleteditems-user-owned.md) | [directoryObject](directoryobject.md) コレクション | ユーザーによって所有されているディレクトリの項目を一覧表示します。 |

## <a name="properties"></a>プロパティ
| プロパティ   | 型 |説明|
|:---------------|:--------|:----------|
|id|String| オブジェクトの一意識別子 (例: 12345678-9abc-def0-1234-56789abcde)。 キー。 null 許容ではありません。 読み取り専用です。|

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|deleteditems|[directoryObject](directoryobject.md) コレクション| 最近削除されたアイテム 読み取り専用。 Null 許容型。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
  "id": "String (identifier)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directory resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->