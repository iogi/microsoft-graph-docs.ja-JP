---
title: mailTipsError リソースの種類
description: 操作中に発生するエラーです。
ms.openlocfilehash: 8604207844ade4e0c10981f30d03b33eacf4a0a2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27021769"
---
# <a name="mailtipserror-resource-type"></a>mailTipsError リソースの種類

操作中に発生するエラーです。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:-----|:-----|:-----|
| message | String | エラー メッセージ。 |
| code | String | エラー コード。 |

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mailTipsError"
}-->

```json
{
  "message": "string",
  "code": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailTipsError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->