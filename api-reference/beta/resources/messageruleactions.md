---
title: messageRuleActions リソースの種類
description: ルールに使用可能なアクションのセットを表します。
ms.openlocfilehash: fbd189d8a43dc47e139f69cd345b4c14744d94f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067273"
---
# <a name="messageruleactions-resource-type"></a>messageRuleActions リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

ルールに使用可能なアクションのセットを表します。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| assignCategories | String コレクション | メッセージに割り当てられるカテゴリの一覧です。 |
| copyToFolder | String | メッセージのコピー先のフォルダーの ID です。 |
| delete | Boolean | 削除済みアイテム フォルダーにメッセージを移動する必要があるかどうかを示します。 |
| forwardAsAttachmentTo | [recipient](recipient.md) コレクション | 添付ファイルとしてメッセージを転送する受信者の電子メール アドレスです。 |
| forwardTo | [recipient](recipient.md) コレクション | メッセージを転送する受信者の電子メール アドレスです。 |
| markAsRead | Boolean | メッセージを開封済みにする必要があるかどうかを示します。 |
| markImportance | String | メッセージの重要度を設定します。使用可能な値は、`low`、`normal`、`high` です。 |
| moveToFolder |  String| メッセージ移動先のフォルダーの ID です。 |
| permanentDelete | Boolean | メッセージを完全に削除し、削除済みアイテム フォルダーにメッセージを保存しないようにするかどうかを示します。 |
| redirectTo | [recipient](recipient.md) | メッセージのリダイレクト先の電子メール アドレスです。 |
| stopProcessingRules | Boolean | 後続のルールを評価する必要があるかどうかを示します。 |


## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRuleActions"
}-->

```json
{
  "assignCategories": ["String"],
  "copyToFolder": "String",
  "delete": "Boolean",
  "forwardAsAttachmentTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "forwardTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "markAsRead": "Boolean",
  "markImportance": "String",
  "moveToFolder": "String",
  "permanentDelete": "Boolean",
  "redirectTo": {"@odata.type": "microsoft.graph.recipient"},
  "stopProcessingRules": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRuleActions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->