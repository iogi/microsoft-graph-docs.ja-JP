# <a name="page-resource-type"></a>page リソースの種類

OneNote ノートブックのページです。

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "@odata.type": "microsoft.graph.onenotePage"
}-->

```json
{
  "content": "stream",
  "contentUrl": "string",
  "createdByAppId": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "level": 1024,
  "links": {"@odata.type": "microsoft.graph.pageLinks"},
  "order": 1024,
  "self": "string",
  "title": "string"
}

```
## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|content|Stream|ページの HTML コンテンツ。|
|contentUrl|String|ページの HTML コンテンツの URL。読み取り専用です。|
|createdByAppId|String|ページを作成したアプリケーションの一意の識別子。読み取り専用です。|
|createdDateTime|DateTimeOffset|ページが作成された日時。Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`読み取り専用です。|
|id|String|ページの一意識別子。読み取り専用です。|
|lastModifiedDateTime|DateTimeOffset|ページが最後に変更された日時。Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`読み取り専用です。|
|level|Int32|ページのインデント レベル。読み取り専用です。|
|links|[PageLinks](pagelinks.md)|ページを開くためのリンク。`oneNoteClientURL`リンクが OneNote のネイティブ クライアントでページを開きます (インストールされている場合)。`oneNoteWebUrl` リンクでは、OneNote オンラインでページを開きます。読み取り専用です。|
|order|Int32|親セクション内でのページの順序。読み取り専用です。|
|self|String|ページに関する詳細情報を入手できるエンドポイント。読み取り専用です。|
|title|String|ページのタイトル。 |

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|parentNotebook|[Notebook](notebook.md)|ページを含むノートブック。読み取り専用です。|
|parentSection|[Section](section.md)|ページを含むセクション。読み取り専用です。|

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Get page](../api/page_get.md) | [Page](page.md) |ページのプロパティとリレーションシップを読み取ります。|
|[Update page content](../api/page_update.md) | なし |ページの HTML コンテンツを更新します。 |
|[Delete page](../api/page_delete.md) | なし |ページを削除します。 |
|[copyToSection](../api/page_copytosection.md)| なし |特定のセクションにページをコピーします。|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->