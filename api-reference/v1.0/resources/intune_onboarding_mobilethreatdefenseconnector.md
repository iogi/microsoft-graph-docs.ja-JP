# <a name="mobilethreatdefenseconnector-resource-type"></a>mobileThreatDefenseConnector リソースの種類

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

Mobile Threat Defense パートナーとの接続を表すエンティティです。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[mobileThreatDefenseConnectors のリスト](../api/intune_onboarding_mobilethreatdefenseconnector_list.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) コレクション|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[mobileThreatDefenseConnector の取得](../api/intune_onboarding_mobilethreatdefenseconnector_get.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[mobileThreatDefenseConnector の作成](../api/intune_onboarding_mobilethreatdefenseconnector_create.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|新しい [mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) オブジェクトを作成します。|
|[mobileThreatDefenseConnector の削除](../api/intune_onboarding_mobilethreatdefenseconnector_delete.md)|なし|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) を削除します。|
|[mobileThreatDefenseConnector の更新](../api/intune_onboarding_mobilethreatdefenseconnector_update.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md)|[mobileThreatDefenseConnector](../resources/intune_onboarding_mobilethreatdefenseconnector.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|まだ文書化されていません|
|lastHeartbeatDateTime|DateTimeOffset|データ同期パートナーから受信した最後のハートビートの日時|
|partnerState|String|このアカウントのデータ同期パートナーの状態です。使用可能な値は、`unavailable`、 `available`、 `enabled`、`unresponsive`です。|
|androidEnabled|ブール型|Android において、準拠評価時にデータ同期パートナーからのデータを使用するかどうかを設定します|
|iosEnabled|ブール型|IOS において、準拠評価時にデータ同期パートナーからのデータを使用するかどうかを取得または設定します|
|androidDeviceBlockedOnMissingPartnerData|ブール型|Android において、デバイスを準拠させる前に Intune がデータ同期パートナーからデータを受信する必要があるかどうかを設定します|
|iosDeviceBlockedOnMissingPartnerData|ブール型|IOS において、デバイスを準拠させる前に Intune がデータ同期パートナーからデータを受信する必要があるかどうかを設定します|
|partnerUnsupportedOsVersionBlocked|ブール型|データ同期パートナーの最小バージョンの要件を満たさない、有効なプラットフォーム上のデバイスをブロックするかどうかを取得または設定します|
|partnerUnresponsivenessThresholdInDays|Int32|このパートナー統合に関する、テナントごとの無応答への許容日数の取得または設定を行います|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileThreatDefenseConnector"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileThreatDefenseConnector",
  "id": "String (identifier)",
  "lastHeartbeatDateTime": "String (timestamp)",
  "partnerState": "String",
  "androidEnabled": true,
  "iosEnabled": true,
  "androidDeviceBlockedOnMissingPartnerData": true,
  "iosDeviceBlockedOnMissingPartnerData": true,
  "partnerUnsupportedOsVersionBlocked": true,
  "partnerUnresponsivenessThresholdInDays": 1024
}
```



