# <a name="devicegeolocation-resource-type"></a>deviceGeoLocation リソースの種類

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

デバイスの場所
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|lastCollectedDateTime|DateTimeOffset|場所が記録された、UTC を基準とする時刻|
|longitude|Double|デバイスの場所の経度座標|
|latitude|Double|デバイスの場所の緯度座標|
|altitude|Double|海抜標高 (メートル単位)|
|horizontalAccuracy|Double|経度と緯度の精度 (メートル単位)|
|verticalAccuracy|Double|標高の精度 (メートル単位)|
|heading|Double|真北を基準とする方角|
|speed|Double|デバイスの移動速度 (m/秒)|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceGeoLocation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceGeoLocation",
  "lastCollectedDateTime": "String (timestamp)",
  "longitude": "<Unknown Primitive Type Edm.Double>",
  "latitude": "<Unknown Primitive Type Edm.Double>",
  "altitude": "<Unknown Primitive Type Edm.Double>",
  "horizontalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "verticalAccuracy": "<Unknown Primitive Type Edm.Double>",
  "heading": "<Unknown Primitive Type Edm.Double>",
  "speed": "<Unknown Primitive Type Edm.Double>"
}
```



