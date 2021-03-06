# plannerAssignments リソースの種類
<a id="plannerassignments-resource-type" class="xliff"></a>

**plannerAssignments** リソースは [plannerTask](plannertask.md) リソースの割り当てを表します。この型はオープン型です。この型の各プロパティ名は、タスクが割り当てられているユーザー オブジェクトの ID です。ユーザーは、orderHint プロパティが値として設定されている [plannerassignment](plannerassignment.md) オブジェクトとそれぞれの ID を使った名前の付いた新しいプロパティを作成して、タスクに割り当てることができます。担当者は、それぞれの ID を使った名前の付いたプロパティを null に設定することによって、タスクからの割り当てを解除できます。


## プロパティ
<a id="properties" class="xliff"></a>
クライアントは、オープン型のプロパティを定義できます。ただしこの場合、クライアントは割り当て済みユーザーの ID をプロパティ名として指定する必要があります。担当者を作成または変更する場合はプロパティを **plannerAssignment** オブジェクトに設定し、削除する場合は null に設定します。

例:

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerAssignments"
}-->

```json
{
  "ca2a1df2-e36b-4987-9f6b-0ea462f4eb47": null,
  "4e98f8f1-bb03-4015-b8e0-19bb370949d8": { 
      "@odata.type": "microsoft.graph.plannerAssignment",
      "orderHint": "String"
    }
}
```
この例では、ID が ca2a1df2-e36b-4987-9f6b-0ea462f4eb47 のユーザーをタスクの担当者リストから削除し、ユーザー ID が 4e98f8f1-bb03-4015-b8e0-19bb370949d8 の担当者の順序を変更します。ID が 4e98f8f1-bb03-4015-b8e0-19bb370949d8 のユーザーにタスクがまだ割り当てられていない場合は、この値を使って割り当てを更新すると、タスクがこのユーザーに割り当てられます。

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerAssignments resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->