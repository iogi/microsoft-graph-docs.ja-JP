# <a name="privacyprofile-resource-type"></a>privacyProfile リソースの種類

会社のプライバシー プロファイルを表します。このプライバシー プロファイルには、プライバシー ステートメントの URL と、プライバシー ステートメントに関する連絡先担当者が含まれます。

## <a name="properties"></a>プロパティ
| プロパティ   | 型|説明|
|:---------------|:--------|:----------|
|contactEmail|String| プライバシー ステートメントの連絡先担当者の有効な SMTP メール アドレス。 省略可。|
|statementUrl|String| http:// または https:// で始まる有効な URL 形式。 最大の長さは 255 文字です。 会社のプライバシー ステートメントに誘導する URL。 省略可。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privacyProfile"
}-->

```json
{
  "contactEmail": "string",
  "statementUrl": "string"
}
```