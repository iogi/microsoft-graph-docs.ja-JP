---
title: governanceSchedule リソースの種類
description: 'GovernanceRoleAssignmentRequest のスケジュールを表します。 役割の割り当て要求のスケジュールを制御、ロールの割り当て操作を実行する場合、役割の割り当てを停止するタイミングと役割の割り当て操作を実行する頻度です。 '
ms.openlocfilehash: 6eff3977aa7806c975f968b8706f2e8c21e5d99e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27071537"
---
# <a name="governanceschedule-resource-type"></a>governanceSchedule リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

の[governanceRoleAssignmentRequest](../resources/governanceroleassignmentrequest.md)のスケジュールを表します。 役割の割り当て要求のスケジュールを制御、ロールの割り当て操作を実行する場合、役割の割り当てを停止するタイミングと役割の割り当て操作を実行する頻度です。 



## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|startDateTime|DateTimeOffset|役割の割り当ての開始時刻。 Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|endDateTime|DateTimeOffset|役割の割り当ての終了時間です。 Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'` *注: 場合は、値は、 `null`、永続的な割り当てを示します。*|
|type|String|ロールの割り当てスケジュールの種類です。 のみ`Once`ここではサポートされています。
|duration|Duration|役割の割り当ての期間です。 TimeSpan の形式であります。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceSchedule"
}-->

```json
{
  "duration": "String (timespan)",
  "startDateTime": "String (timestamp)",
  "endDateTime": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceSchedule",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->