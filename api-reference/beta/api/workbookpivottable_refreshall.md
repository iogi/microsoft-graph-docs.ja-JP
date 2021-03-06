# <a name="workbookpivottable-refreshall"></a>workbookPivotTable: refreshAll

指定されたワークシート内のピボットテーブルを更新します。

### <a name="prerequisites"></a>前提条件
この API を実行するために必要な**スコープ**は、次のとおりです。_Files.Read、Files.ReadWrite_
### <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/root/workbook/worksheets/{id}/pivotTables/refreshAll

```
### <a name="request-headers"></a>要求ヘッダー
| 名前       | 説明|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | 変更を保持するかどうかを決定するブック セッション ID。省略可能。|

### <a name="request-body"></a>要求本文

### <a name="response"></a>応答
成功した場合、このメソッドは `200, OK` 応答コードを返します。応答本文には何も返されません。

### <a name="example"></a>例
以下は、この API を呼び出す方法の例です。
##### <a name="request"></a>要求
以下は、要求の例です。
<!-- {
  "blockType": "request",
  "name": "workbookpivottable_refreshall"
}-->
```http
POST https://graph.microsoft.com/{ver}/drive/root/workbook/worksheets/{id}/pivotTables/refreshAll
```

##### <a name="response"></a>応答
以下は、応答の例です。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.none"
} -->
```http
HTTP/1.1 200 OK
```
