# <a name="get-workbookpivottable"></a>workbookPivotTable を取得する

worksheetprotection オブジェクトのプロパティとリレーションシップを取得します。

### <a name="prerequisites"></a>前提条件
この API を実行するために必要な**スコープ**は、次のとおりです。_Files.Read、Files.ReadWrite_

### <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/root/workbook/worksheets/{id}/pivotTables/{id}
```
### <a name="optional-query-parameters"></a>オプションのクエリ パラメーター
このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)をサポートします。

### <a name="request-headers"></a>要求ヘッダー
| 名前      |説明|
|:----------|:----------|
| Authorization  | Bearer <code>|
| Workbook-Session-Id  | 変更を保持するかどうかを決定するブック セッション ID。省略可能。|

### <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。
### <a name="response"></a>応答
成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [workbookPivotTable](../resources/workbookpivottable.md) オブジェクトを返します。
### <a name="example"></a>例
##### <a name="request"></a>要求
以下は、要求の例です。
<!-- {
  "blockType": "request",
  "name": "get_workbookpivottable"
}-->
```http
GET https://graph.microsoft.com/{ver}/drive/root/workbook/worksheets/{id}/pivotTables/{id}
```
##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookPivotTable"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 46

{
  "id": "id-value",
  "name": "name-value"
}
```
