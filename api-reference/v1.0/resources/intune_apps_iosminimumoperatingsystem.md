# <a name="iosminimumoperatingsystem-resource-type"></a>iosMinimumOperatingSystem リソースの種類

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

iOS モバイル アプリに必要な最小限のオペレーティング システムのプロパティが含まれます。
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|v8_0|ブール型 (Boolean)|バージョン 8.0 以降。|
|v9_0|ブール型 (Boolean)|バージョン 9.0 以降。|
|v10_0|ブール型 (Boolean)|バージョン 10.0 以降。|
|v11_0|ブール型 (Boolean)|バージョン 11.0 以降。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMinimumOperatingSystem",
  "v8_0": true,
  "v9_0": true,
  "v10_0": true,
  "v11_0": true
}
```



