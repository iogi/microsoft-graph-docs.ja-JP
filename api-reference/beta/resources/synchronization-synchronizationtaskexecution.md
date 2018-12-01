---
title: synchronizationTaskExecution リソースの種類
description: 同期ジョブの実行の結果をまとめたものです。
ms.openlocfilehash: 4aefba4bdf9ab850892344e6e34683e81d1a1afa
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27070245"
---
# <a name="synchronizationtaskexecution-resource-type"></a>synchronizationTaskExecution リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

同期ジョブの実行の結果をまとめたものです。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|activityIdentifier           |String |実行ジョブの識別子です。|
|countEntitled                |Int64  |このアプリケーションに割り当てられた処理されたエントリの数。|
|countEntitledForProvisioning |Int64  |プロビジョニング用に割り当てられた処理されたエントリの数。|
|countEscrowed                |Int64  |Escrowed (エラー) のエントリの数。|
|countEscrowedRaw             |Int64  |Escrows のシステムで生成されたを含む、escrowed されたエントリの数。|
|countExported                |Int64  |エクスポートされたエントリの数。|
|countExports                 |Int64  |エクスポートする必要があるエントリの数です。|
|countImported                |Int64  |インポートされたエントリの数。|
|countImportedDeltas          |Int64  |インポートの差分変更の数です。|
|countImportedReferenceDeltas |Int64  |参照の変更に関連するインポートされたデルタの変更の数です。|
|エラー                        |[synchronizationError](synchronization-synchronizationerror.md)|エラーが発生した場合に、詳細を含む、 **synchronizationError**オブジェクトが含まれています。|
|state                        |String |コードがこの実行の結果を要約します。 可能な値は、`Succeeded`、`Failed`、`EntryLevelErrors` です。|
|timeBegan                    |DateTimeOffset|このジョブの実行を開始したときの時間です。 Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|timeEnded                    |DateTimeOffset|このジョブを実行すると時間が終了しました。 Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationTaskExecution"
}-->

```json
{
  "activityIdentifier": "String",
  "countEntitled": 1024,
  "countEntitledForProvisioning": 1024,
  "countEscrowed": 1024,
  "countEscrowedRaw": 1024,
  "countExported": 1024,
  "countExports": 1024,
  "countImported": 1024,
  "countImportedDeltas": 1024,
  "countImportedReferenceDeltas": 1024,
  "error": {"@odata.type": "microsoft.graph.synchronizationError"},
  "state": "String",
  "timeBegan": "String (timestamp)",
  "timeEnded": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationTaskExecution resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->