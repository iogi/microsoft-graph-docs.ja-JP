# <a name="iosmanagedappprotection-resource-type"></a>iosManagedAppProtection リソース タイプ

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

iOS デバイス上の特定のセキュリティ グループおよびアプリの特定のセットを対象とした、管理設定の詳細を構成するために使用するポリシー

[targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List iosManagedAppProtections](../api/intune_mam_iosmanagedappprotection_list.md)|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) コレクション|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get iosManagedAppProtection](../api/intune_mam_iosmanagedappprotection_get.md)|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md)|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create iosManagedAppProtection](../api/intune_mam_iosmanagedappprotection_create.md)|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md)|新しい [iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) オブジェクトを作成します。|
|[Delete iosManagedAppProtection](../api/intune_mam_iosmanagedappprotection_delete.md)|なし|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) を削除します。|
|[Update iosManagedAppProtection](../api/intune_mam_iosmanagedappprotection_update.md)|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md)|[iosManagedAppProtection](../resources/intune_mam_iosmanagedappprotection.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|displayName|String|ポリシーの表示名。 [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します|
|description|String|ポリシーの説明。 [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します|
|createdDateTime|DateTimeOffset|ポリシーが作成された日時。 [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|ポリシーが変更された最終日時。 [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します|
|id|String|エンティティのキー。 [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します|
|version|String|エンティティのバージョン。 [managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します|
|periodOfflineBeforeAccessCheck|Duration|デバイスがインターネットに接続されていないでこの期間が過ぎると、アクセスがチェックされます。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|periodOnlineBeforeAccessCheck|Duration|デバイスがインターネットに接続されていてこの期間が過ぎると、アクセスがチェックされます。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|allowedInboundDataTransferSources|String|データの転送が許可されたソース。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します。可能な値は、`allApps`、`managedApps`、`none` です。|
|allowedOutboundDataTransferDestinations|String|データの転送が許可された宛先。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します。可能な値は、`allApps`、`managedApps`、`none` です。|
|organizationalCredentialsRequired|Boolean|アプリを使用するために組織の資格情報が必要かどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|allowedOutboundClipboardSharingLevel|String|管理対象デバイスで、アプリ間でクリップボードを共有できるレベル。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します。可能な値は、`allApps`、`managedAppsWithPasteIn`、`managedApps`、`blocked` です。|
|dataBackupBlocked|Boolean|管理対象アプリのデータのバックアップがブロックされるかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|deviceComplianceRequired|Boolean|デバイスの準拠が必要かどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|managedBrowserToOpenLinksRequired|Boolean|管理対象ブラウザー アプリでインターネット リンクを開く必要があるかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|saveAsBlocked|Boolean|ユーザーが保護されたファイルのコピーを保存するために、[名前を付けて保存] メニュー項目を使用できるかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|periodOfflineBeforeWipeIsEnforced|Duration|アプリがインターネットから切断されている状態を維持できる時間数。この時間を過ぎると管理対象データはすべて消去されます。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|pinRequired|Boolean|アプリ レベルの pin が必要かどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|maximumPinRetries|Int32|正しくない pin の再試行の最大回数。この回数を超えると管理対象アプリが消去されます。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|simplePinBlocked|Boolean|simplePin がブロックされるかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|minimumPinLength|Int32|PinRequired が True に設定されている場合の、アプリ レベルの pin に必要な最小限の pin の長さ ([managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承)|
|pinCharacterSet|String|PinRequired が True に設定されている場合に、アプリ レベルの pin に使用できる文字セット。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します。可能な値は、`numeric`、`alphanumericAndSymbol` です。|
|periodBeforePinReset|Duration|PinRequired が True に設定されている場合、この TimePeriod を過ぎると全レベルの pin を再設定する必要があります。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|allowedDataStorageLocations|String コレクション|ユーザーが管理対象データを格納できるデータの保存場所。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|contactSyncBlocked|Boolean|連絡先をユーザー デバイスに同期できるかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|printBlocked|Boolean|管理対象アプリからの印刷を許可するかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|fingerprintBlocked|Boolean|PinRequired が True に設定されている場合に、pin の代わりに指紋リーダーの使用を許可するかどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|disableAppPinIfDevicePinIsSet|Boolean|デバイスの pin が設定されている場合に、アプリの pin の使用が必要かどうかを示します。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|minimumRequiredOsVersion|String|バージョンが、指定されたバージョンよりも小さい場合に、管理対象アプリによる会社のデータへのアクセスをブロックします。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|minimumWarningOsVersion|String|OS のバージョンが、指定されたバージョンよりも小さい場合に、会社のデータへアクセスすると管理対象アプリに警告メッセージが表示されます。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|minimumRequiredAppVersion|String|バージョンが、指定されたバージョンよりも小さい場合に、管理対象アプリによる会社のデータへのアクセスをブロックします。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|minimumWarningAppVersion|String|アプリのバージョンが、指定されたバージョンよりも小さい場合に、管理対象アプリに警告メッセージが表示されます。 [managedAppProtection](../resources/intune_mam_managedappprotection.md) から継承します|
|isAssigned|Boolean|包含グループにポリシーを配置するかどうかを示します。 [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md) から継承します|
|appDataEncryptionType|String|管理対象アプリのデータに使用する暗号化の種類。 可能な値は、`useDeviceSettings`、`afterDeviceRestart`、`whenDeviceLockedExceptOpenFiles`、`whenDeviceLocked` です。|
|minimumRequiredSdkVersion|String|バージョンが、指定されたバージョンよりも小さい場合に、管理対象アプリによる会社のデータへのアクセスをブロックします。|
|deployedAppCount|Int32|現在のポリシーが配置されたアプリの数。|
|faceIdBlocked|Boolean|PinRequired が True に設定されている場合に、pin の代わりに FaceID の使用を許可するかどうかを示します。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|assignments|targetedManagedAppPolicyAssignment コレクション|ポリシーが配置される包含グループと除外グループのリストのナビゲーション プロパティです。 [targetedManagedAppProtection](../resources/intune_mam_targetedmanagedappprotection.md) から継承します|
|apps|[managedMobileApp](../resources/intune_mam_managedmobileapp.md) コレクション|ポリシーが配置されたアプリのリスト。|
|deploymentSummary|[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md)|構成の展開概要のナビゲーション プロパティ。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosManagedAppProtection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosManagedAppProtection",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String",
  "periodOfflineBeforeAccessCheck": "String (duration)",
  "periodOnlineBeforeAccessCheck": "String (duration)",
  "allowedInboundDataTransferSources": "String",
  "allowedOutboundDataTransferDestinations": "String",
  "organizationalCredentialsRequired": true,
  "allowedOutboundClipboardSharingLevel": "String",
  "dataBackupBlocked": true,
  "deviceComplianceRequired": true,
  "managedBrowserToOpenLinksRequired": true,
  "saveAsBlocked": true,
  "periodOfflineBeforeWipeIsEnforced": "String (duration)",
  "pinRequired": true,
  "maximumPinRetries": 1024,
  "simplePinBlocked": true,
  "minimumPinLength": 1024,
  "pinCharacterSet": "String",
  "periodBeforePinReset": "String (duration)",
  "allowedDataStorageLocations": [
    "String"
  ],
  "contactSyncBlocked": true,
  "printBlocked": true,
  "fingerprintBlocked": true,
  "disableAppPinIfDevicePinIsSet": true,
  "minimumRequiredOsVersion": "String",
  "minimumWarningOsVersion": "String",
  "minimumRequiredAppVersion": "String",
  "minimumWarningAppVersion": "String",
  "isAssigned": true,
  "appDataEncryptionType": "String",
  "minimumRequiredSdkVersion": "String",
  "deployedAppCount": 1024,
  "faceIdBlocked": true
}
```



