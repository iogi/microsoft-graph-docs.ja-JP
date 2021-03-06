# <a name="section-resource-type"></a>section リソースの種類

OneNote ノートブックのセクションです。セクションには、ページを含めることができます。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "pages",
    "parentNotebook",
    "parentSectionGroup"
  ],
  "@odata.type": "microsoft.graph.onenoteSection"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.sectionLinks"},
  "displayName": "string",
  "pagesUrl": "string",
  "self": "string"
}

```
## <a name="properties"></a>プロパティ
| プロパティ       | 型    |説明|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|そのアイテムを作成したユーザーの ID、デバイス、アプリケーション。読み取り専用です。|
|createdDateTime|DateTimeOffset|セクションが作成された日時。Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`読み取り専用です。|
|id|String|セクションの一意識別子。読み取り専用です。|
|isDefault|ブール型|これがユーザーの既定のセクションであるかどうかを示します。読み取り専用です。|
|lastModifiedBy|[identitySet](identityset.md)|そのアイテムを作成したユーザーの ID、デバイス、アプリケーション。読み取り専用です。|
|lastModifiedDateTime|DateTimeOffset|セクションが最後に変更された日時。Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`読み取り専用です。|
|links|[SectionLinks](sectionlinks.md)|セクションを開くためのリンク。`oneNoteClientURL` リンクが OneNote のネイティブ クライアントでセクションを開きます (インストールされている場合)。`oneNoteWebURL` リンクでは、OneNote Online でセクションを開きます。|
|displayName|String|セクションの名前。 |
|pagesUrl|String|セクション内のすべてのページに関する詳細情報を入手できる `pages` エンドポイント。読み取り専用です。|
|self|String|セクションに関する詳細情報を入手できるエンドポイント。読み取り専用です。|

## <a name="relationships"></a>関係
| リレーションシップ | 型    |説明|
|:---------------|:--------|:----------|
|pages|[Page](page.md) コレクション|セクション内のページのコレクションです。読み取り専用です。Null 許容型。|
|parentNotebook|[Notebook](notebook.md)|セクションを含むノートブック。読み取り専用です。|
|parentSectionGroup|[SectionGroup](sectiongroup.md)|セクションを含むセクション グループ。読み取り専用です。|

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Get section](../api/section_get.md) | [Section](section.md) |セクションのプロパティとリレーションシップを読み取ります。|
|[Create page](../api/section_post_pages.md) |[Page](page.md)| 指定されたセクションでページのコレクションに投稿してページを作成します。|
|[List pages](../api/section_list_pages.md) |[Page](page.md) コレクション| 指定されたセクション内のページのコレクションを取得します。|
|[copyToNotebook](../api/section_copytonotebook.md)|なし|特定のノートブックにセクションをコピーします。|
|[copyToSectionGroup](../api/section_copytosectiongroup.md)|なし|特定のセクション グループにセクションをコピーします。|


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
