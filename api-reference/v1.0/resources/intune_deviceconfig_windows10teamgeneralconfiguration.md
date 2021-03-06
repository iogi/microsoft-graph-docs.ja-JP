# <a name="windows10teamgeneralconfiguration-resource-type"></a>windows10TeamGeneralConfiguration リソース タイプ

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

このトピックでは、windows10TeamGeneralConfiguration リソースによって公開された、宣言されたメソッド、プロパティ、リレーションシップについて説明します。

[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List windows10TeamGeneralConfigurations](../api/intune_deviceconfig_windows10teamgeneralconfiguration_list.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) コレクション|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_get.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_create.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|新しい [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) オブジェクトを作成します。|
|[Delete windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_delete.md)|なし|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) を削除します。|
|[Update windows10TeamGeneralConfiguration](../api/intune_deviceconfig_windows10teamgeneralconfiguration_update.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md)|[windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|オブジェクトが最後に変更された DateTime。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|createdDateTime|DateTimeOffset|オブジェクトが作成された DateTime。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|description|String|デバイス構成について管理者が提供した説明。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|displayName|String|デバイス構成について管理者が指定した名前。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|version|Int32|デバイス構成のバージョン。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|azureOperationalInsightsBlockTelemetry|Boolean|Azure Operational Insights をブロックするかどうかを示します。|
|azureOperationalInsightsWorkspaceId|String|Azure Operational Insights のワークスペース ID。|
|azureOperationalInsightsWorkspaceKey|String|Azure Operational Insights のワークスペース キー。|
|connectAppBlockAutoLaunch|Boolean|投影を開始するたびに、接続アプリを自動的に起動するかどうかを指定します。|
|maintenanceWindowBlocked|Boolean|デバイス更新のメンテナンス ウィンドウの設定をブロックするかどうかを示します。|
|maintenanceWindowDurationInHours|Int32|デバイス更新のためのメンテナンス ウインドウの期間。 有効な値は 0 から 5 までです|
|maintenanceWindowStartTime|TimeOfDay|デバイス更新のためのメンテナンス ウィンドウの開始時刻。|
|miracastChannel|String|チャネル。 可能な値は、`userDefined`、`one`、`two`、`three`、`four`、`five`、`six`、`seven`、`eight`、`nine`、`ten`、`eleven`、`thirtySix`、`forty`、`fortyFour`、`fortyEight`、`oneHundredFortyNine`、`oneHundredFiftyThree`、`oneHundredFiftySeven`、`oneHundredSixtyOne`、`oneHundredSixtyFive` です。|
|miracastBlocked|Boolean|ワイヤレス投影をブロックするかどうかを示します。|
|miracastRequirePin|Boolean|ワイヤレス投影の pin が必要かどうかを示します。|
|settingsBlockMyMeetingsAndFiles|Boolean|スタート メニューで [会議とファイル] 機能を無効にするかどうかを指定します。この機能は、サインイン ユーザーの会議とファイルを Office 365 から表示します。|
|settingsBlockSessionResume|Boolean|セッションがタイムアウトになった際にセッションを再開する機能を許可するかどうかを指定します。|
|settingsBlockSigninSuggestions|Boolean|スケジュールされている会議の招待者をサインイン ダイアログに自動入力する機能を無効にするかどうかを指定します。|
|settingsDefaultVolume|Int32|新しいセッションの既定のボリューム値を指定します。 許可される値は、0 から 100 までです。 既定値は 45 です。 有効な値は 0 から 100 までです|
|settingsScreenTimeoutInMinutes|Int32|ハブ スクリーンがオフになるまでの分数を指定します。|
|settingsSessionTimeoutInMinutes|Int32|セッションがタイムアウトになるまでの分数を指定します。|
|settingsSleepTimeoutInMinutes|Int32|ハブがスリープ モードになるまでの分数を指定します。|
|welcomeScreenBlockAutomaticWakeUp|Boolean|ユーザーが入室した際に、ようこそ画面が自動的に起動するのをブロックするかどうかを指定します。|
|welcomeScreenBackgroundImageUrl|String|ようこそ画面の背景画像の URL。 URL は HTTPS プロトコルを使用し、PNG 画像を返す必要があります。|
|welcomeScreenMeetingInformation|String|表示される、ようこそ画面の会議情報。 可能な値は、`userDefined`、`showOrganizerAndTimeOnly`、`showOrganizerAndTimeAndSubject` です。|

## <a name="relationships"></a>関係
|リレーションシップ|型|説明|
|:---|:---|:---|
|assignments|[deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md) コレクション|デバイスの構成プロファイルの割り当てのリスト。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|deviceStatuses|[deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) コレクション|デバイスごとのデバイス構成のインストール状況。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|userStatuses|[deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) コレクション|ユーザーごとのデバイス構成のインストール状況。 [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|デバイス構成のデバイス状態の概要 ([deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md)|デバイス構成のユーザー状態の概要 ([deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承)|
|deviceSettingStateSummaries|[settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md) コレクション|デバイス構成設定状態のデバイスの要約 ([deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承)|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10TeamGeneralConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "String",
  "azureOperationalInsightsWorkspaceKey": "String",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 1024,
  "maintenanceWindowStartTime": "String (time of day)",
  "miracastChannel": "String",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 1024,
  "settingsScreenTimeoutInMinutes": 1024,
  "settingsSessionTimeoutInMinutes": 1024,
  "settingsSleepTimeoutInMinutes": 1024,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "String",
  "welcomeScreenMeetingInformation": "String"
}
```



