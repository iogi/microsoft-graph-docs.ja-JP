# <a name="sectiongroup-resource-type"></a>sectionGroup リソースの種類

OneNote ノートブックのセクション グループ。セクション グループには、セクションとセクション グループを含めることができます。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSectionGroup",
    "sectionGroups",
    "sections"
  ],
  "@odata.type": "microsoft.graph.sectiongroup"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "string",
  "sectionGroupsUrl": "string",
  "sectionsUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a>プロパティ
| プロパティ       | 型    |説明|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|そのアイテムを作成したユーザーの ID、デバイス、アプリケーション。読み取り専用です。|
|createdDateTime|DateTimeOffset|セクション グループが作成された日時。Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`読み取り専用です。|
|id|String|セクション グループの一意識別子。読み取り専用です。|
|lastModifiedBy|[identitySet](identityset.md)|そのアイテムを作成したユーザーの ID、デバイス、アプリケーション。読み取り専用です。| 
|lastModifiedDateTime|DateTimeOffset|セクション グループが最後に変更された日時。Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`読み取り専用です。|
|displayName|String|セクション グループの名前。|
|sectionGroupsUrl|String|セクション グループ内のすべてのセクション グループを返す `sectionGroups` ナビゲーション プロパティの URL。読み取り専用です。| 
|sectionsUrl|String|セクション グループ内のすべてのセクションを返す `sections` ナビゲーション プロパティの URL。読み取り専用です。|
|self|String|セクション グループに関する詳細情報を入手できるエンドポイント。読み取り専用です。|

## <a name="relationships"></a>関係
| リレーションシップ | 型    |説明|
|:---------------|:--------|:----------|
|parentNotebook|[Notebook](notebook.md)|セクション グループを含むノートブック。読み取り専用です。|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|セクション グループを含むセクション グループ。読み取り専用です。|
|sectionGroups|[SectionGroup](sectiongroup.md) コレクション|セクション内のセクション グループ。読み取り専用です。Null 許容型。|
|sections|[Section](section.md) コレクション|セクション グループ内のセクション。読み取り専用です。Null 許容型。|

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Get section group](../api/sectiongroup_get.md) | [SectionGroup](sectiongroup.md) |セクション グループのプロパティとリレーションシップを読み取ります。|
|[Create section group](../api/sectiongroup_post_sectiongroups.md) |[SectionGroup](sectiongroup.md)| 指定したセクション グループで sectionGroup コレクションに投稿してセクション グループを作成します。|
|[List section groups](../api/sectiongroup_list_sectiongroups.md) |[SectionGroup](sectiongroup.md) コレクション| 指定されたセクション グループ内のセクション グループのコレクションを取得します。|
|[Create section](../api/sectiongroup_post_sections.md) |[Section](section.md)| 指定されたセクション グループでセクションのコレクションを投稿してセクションを作成します。|
|[List sections](../api/sectiongroup_list_sections.md) |[Section](section.md) コレクション| 指定されたセクション グループ内のセクションのコレクションを取得します。|


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sectionGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
