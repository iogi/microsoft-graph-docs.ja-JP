# plannerBucketTaskBoardTaskFormat リソースの種類
<a id="plannerbuckettaskboardtaskformat-resource-type" class="xliff"></a>

**plannerBucketTaskBoardTaskFormat** リソースは、タスク ボードのバケット ビューでタスクを正しく表示するための情報を示します (ビューは割り当てられているバケット内のタスクごとに整理されます)。各 [task](plannertask.md) にはそれぞれ **plannerBucketTaskBoardTaskFormat** オブジェクトが 1 つ関連付けられています。


## メソッド
<a id="methods" class="xliff"></a>

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[plannerBucketTaskBoardTaskFormat の取得](../api/plannerbuckettaskboardtaskformat_get.md) | [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md) |**plannerBucketTaskBoardTaskFormat** オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Update](../api/plannerbuckettaskboardtaskformat_update.md) | [plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md)  |**plannerBucketTaskBoardTaskFormat** オブジェクトを更新します。 |

## プロパティ
<a id="properties" class="xliff"></a>
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|String| 読み取り専用です。リソースの ID。28 文字長で、大文字と小文字の区別があります。[書式検証](planner_identifiers_disclaimer.md)はサービスによって行われます。|
|orderHint|String|タスク ボードのバケット ビューでタスクの順序付けに使用するヒント。形式は[ここ](planner_order_hint_format.md)の説明に従って定義されます。|

## リレーションシップ
<a id="relationships" class="xliff"></a>
なし


## JSON 表記
<a id="json-representation" class="xliff"></a>
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerBucketTaskBoardTaskFormat"
}-->

```json
{
  "id": "String (identifier)",
  "orderHint": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerBucketTaskBoardTaskFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->