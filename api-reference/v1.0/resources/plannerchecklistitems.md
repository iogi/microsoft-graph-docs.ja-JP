# plannerChecklistItems リソースの種類
<a id="plannerchecklistitems-resource-type" class="xliff"></a>

**plannerChecklistItemCollection** リソースは、タスクのチェックリスト項目のコレクションを表します。これは、オープン型です。[タスクの詳細](plannertaskdetails.md)オブジェクトの一部です。プロパティ/値の組の値は、[checklistItem](plannerchecklistitem.md) オブジェクトです。


## プロパティ
<a id="properties" class="xliff"></a>
クライアントは、オープン型のプロパティを定義できます。この場合、クライアントは **GUID** をプロパティとして指定し、その値は [checklistItem](plannerchecklistitem.md) オブジェクトでなければなりません。以下に例を示します。チェックリストの項目を削除するには、プロパティの値を `null` に設定します。

## JSON 表記
<a id="json-representation" class="xliff"></a>

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerChecklistItems"
}-->

```json
{
  "String-value":
  {
    "isChecked": true,
    "lastModifiedBy": "String-value",
    "lastModifiedByDateTime": "String(timestamp)",
    "orderHint": "String-value",
    "title": "String-value"
  }
}
```
// 例

```json
{
  "3a73c9dd-fb47-4230-9c0f-b80788fb0f9b": // client-generated GUID
  {
    "@odata.type": "microsoft.graph.checklistItem", // required in PATCH requests to edit the checklist on a task
    "isChecked": true,
    "lastModifiedBy": {
      "user": {
        "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
      }
    },
    "lastModifiedByDateTime": "2015-09-21T17:45:12.039Z",
    "orderHint": "0009005756397228702",
    "title": "Get stamps"
  },
  "5f36f5b2-1ec0-4c48-9c75-ed59429516c5":
  {
     "@odata.type": "microsoft.graph.checklistItem",
    "isChecked": false,
    "lastModifiedBy": {
      "user": {
        "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
      }
    },
    "lastModifiedByDateTime": "2015-09-21T17:45:12.039Z",
    "orderHint": "0004105723397228784",
    "title": "Mail card at UPS"
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerChecklistItems resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->