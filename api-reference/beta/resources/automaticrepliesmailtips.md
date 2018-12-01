---
title: automaticRepliesMailTips リソースの種類
description: メールボックスに設定されているすべての自動返信のメール ヒントです。
ms.openlocfilehash: 51657578474710d40cfc3feabdf41e50e7105942
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27074224"
---
# <a name="automaticrepliesmailtips-resource-type"></a>automaticRepliesMailTips リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

メールボックスに設定されているすべての自動返信の[メール ヒント](../resources/mailtips.md)にします。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:-----|:-----|:-----|
| message | String | 自動応答メッセージ。 |
| messageLanguage | [localeInfo](../resources/localeinfo.md) | 自動応答メッセージの言語。 |
| scheduledEndTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | 自動応答を終了する日時。 |
| scheduledStartTime | [dateTimeTimeZone](../resources/datetimetimezone.md) | 自動応答を開始する日時。 |

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "messageLanguage",
    "scheduledEndTime",
    "scheduledStartTime"
  ],
  "@odata.type": "microsoft.graph.automaticRepliesMailTips"
}-->

```json
{
  "message": "string",
  "messageLanguage": {"@odata.type": "microsoft.graph.localeInfo"},
  "scheduledEndTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesMailTips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->