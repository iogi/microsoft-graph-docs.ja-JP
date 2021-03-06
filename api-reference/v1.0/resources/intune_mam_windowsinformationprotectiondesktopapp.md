# <a name="windowsinformationprotectiondesktopapp-resource-type"></a>windowsInformationProtectionDesktopApp リソースの種類

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

Windows 情報保護用デスクトップ アプリ

[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) からの継承

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|displayName|文字列型 (String)|アプリの表示名。 [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) からの継承|
|description|文字列型 (String)|アプリの説明。 [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) からの継承|
|publisherName|文字列型 (String)|[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) から継承される発行元名|
|productName|文字列型 (String)|製品名。 [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) からの継承|
|denied|ブール型 (Boolean)|true の場合、アプリは拒否された保護または除外です。 [windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) からの継承|
|binaryName|文字列型 (String)|バイナリの名前。|
|binaryVersionLow|文字列型 (String)|下位のバイナリ バージョン。|
|binaryVersionHigh|文字列型 (String)|上位のバイナリ バージョン。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsInformationProtectionDesktopApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionDesktopApp",
  "displayName": "String",
  "description": "String",
  "publisherName": "String",
  "productName": "String",
  "denied": true,
  "binaryName": "String",
  "binaryVersionLow": "String",
  "binaryVersionHigh": "String"
}
```



