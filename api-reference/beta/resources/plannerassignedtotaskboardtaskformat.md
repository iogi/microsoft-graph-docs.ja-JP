---
title: plannerAssignedToTaskBoardTaskFormat リソースの種類
description: '**PlannerAssignedToTaskBoardTaskFormat** リソースは、タスク ボードの AssignedTo ビューを正しく表示するための情報を示します (ビューはタスクが割り当てられているユーザーごとに整理されます)。各 task にはそれぞれ **plannerAssignedToTaskBoardTaskFormat** オブジェクトが 1 つ関連付けられています。'
ms.openlocfilehash: 8fc96d6fa7d4f05f6bc81f7030ebe766bf769e40
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27070624"
---
# <a name="plannerassignedtotaskboardtaskformat-resource-type"></a>plannerAssignedToTaskBoardTaskFormat リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

**PlannerAssignedToTaskBoardTaskFormat** リソースは、タスク ボードの AssignedTo ビューを正しく表示するための情報を示します (ビューはタスクが割り当てられているユーザーごとに整理されます)。各 [task](plannertask.md) にはそれぞれ **plannerAssignedToTaskBoardTaskFormat** オブジェクトが 1 つ関連付けられています。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Get plannerAssignedToTaskBoardTaskFormat](../api/plannerassignedtotaskboardtaskformat-get.md) | [plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md) |**plannerAssignedToTaskBoardTaskFormat** オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Update](../api/plannerassignedtotaskboardtaskformat-update.md) | [plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md)  |**plannerAssignedToTaskBoardTaskFormat** オブジェクトを更新します。 |

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|String| 読み取り専用。 リソースの ID です。 28 の文字、大文字小文字を区別することをお勧めします。 サービスの[フォーマットの検証](tasks-identifiers-disclaimer.md)が行われます。|
|orderHintsByAssignee|[plannerOrderHintsByAssignee](plannerorderhintsbyassignee.md)|タスク ボードの AssignedTo ビューでのタスクの順序付けに使用するヒントのディクショナリ。各エントリのキーは、タスクが割り当てられているユーザーのいずれかであり、値は順序のヒントです。それぞれの値の形式は[ここ](planner-order-hint-format.md)で説明するとおり定義されます。|
|unassignedOrderHint|String|タスクが誰にも割り当てられていない場合、または orderHintsByAssignee ディクショナリに、タスクが割り当てられているユーザーのヒントの順序が指定されない場合に、タスク ボードの AssignedTo ビューでのタスクの順序付けに使用するヒントの値。形式は[ここ](planner-order-hint-format.md)の説明に従って定義されます。|

## <a name="relationships"></a>リレーションシップ
なし


## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignedToTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHintsByAssignee": {"@odata.type": "microsoft.graph.plannerOrderHintsByAssignee"},
  "unassignedOrderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignedToTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->