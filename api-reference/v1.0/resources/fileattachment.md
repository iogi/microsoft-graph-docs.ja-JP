# <a name="fileattachment-resource-type"></a>fileAttachment リソースの種類

イベント、メッセージまたは投稿に添付されたファイル (テキスト ファイルや Word 文書など) です。**contentBytes** プロパティには、base64 でエンコードされたファイルの内容が含まれています。  

添付ファイルを作成する場合は、要求本文に以下が含まれます。

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* 必要なプロパティ **name** と **contentBytes**。

[添付ファイル](attachment.md)から派生します。

## <a name="methods"></a>メソッド

| メソッド       | 戻り値の型  |説明|
|:---------------|:--------|:----------|
|[取得](../api/attachment_get.md) | [fileAttachment](fileattachment.md) |fileattachment オブジェクトのプロパティと関係を読み取ります。|
|[Delete](../api/attachment_delete.md) | なし |fileAttachment オブジェクトを削除します。 |

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|contentBytes|Binary|base64 でエンコードされたファイルの内容。|
|contentId|String|Exchange ストア内の添付ファイルの ID。|
|contentLocation|String|添付ファイルのコンテンツの場所に対応する Uniform Resource Identifier (URI)。|
|contentType|String|添付ファイルのコンテンツ タイプ。|
|id|String|添付ファイル ID。|
|isInline|Boolean|インライン添付ファイルの場合、true に設定します。|
|lastModifiedDateTime|DateTimeOffset|添付ファイルが最後に変更された日時です。|
|name|String|埋め込み添付ファイルを表すアイコンの下に表示されるテキストを表す名前。これは、実際のファイル名にする必要はありません。|
|size|Int32|添付ファイルのバイト単位のサイズ。|

## <a name="relationships"></a>関係
なし


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileAttachment"
}-->

```json
{
  "contentBytes": "binary",
  "contentId": "string",
  "contentLocation": "string",
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
