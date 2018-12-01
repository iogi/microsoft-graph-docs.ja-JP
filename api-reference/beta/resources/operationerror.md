---
title: operationError リソースの種類
description: TeamsAsyncOperation で発生したエラーをについて説明します。
ms.openlocfilehash: 0207f490328d377fedab72d2a5300baaf3645150
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068654"
---
# <a name="operationerror-resource-type"></a>operationError リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

[TeamsAsyncOperation](teamsasyncoperation.md)で発生したエラーをについて説明します。

## <a name="operationerror-properties"></a>operationError プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|code|文字列 (読み取り専用)|操作のエラー コードです。|
|message|文字列 (読み取り専用)|エラー メッセージを操作します。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.operationError"
}-->

```json
{
    "code": "TeamUnavailable",
    "message": "The team was not found."
}
```

<!-- uuid: 069fadaa-52db-4ced-85d5-74f7caa2c66f
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation error resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->