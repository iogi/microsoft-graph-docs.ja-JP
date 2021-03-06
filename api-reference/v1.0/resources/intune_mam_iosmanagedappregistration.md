# <a name="iosmanagedappregistration-resource-type"></a>iosManagedAppRegistration リソースの種類

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

特定のユーザーに対する、iOS アプリの管理機能との同期の詳細を示します。
ManagedAppRegistration リソースは、組織のメンバーに使用されるアプリの詳細を管理機能と共に示します。

[managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[iosManagedAppRegistrations のリスト](../api/intune_mam_iosmanagedappregistration_list.md)|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md) コレクション|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[iosManagedAppRegistration の取得](../api/intune_mam_iosmanagedappregistration_get.md)|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md)|[iosManagedAppRegistration](../resources/intune_mam_iosmanagedappregistration.md) オブジェクトのプロパティとリレーションシップを読み取ります。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|createdDateTime|DateTimeOffset|作成日時 ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)。|
|lastSyncDateTime|DateTimeOffset|アプリが管理サービスと最後に同期した日時。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|
|applicationVersion|String|アプリのバージョン ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|managementSdkVersion|String|アプリ管理 SDK のバージョン ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|platformVersion|String|オペレーティング システムのバージョン ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|deviceType|String|ホスト デバイスの種類 ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|deviceTag|String|アプリ管理 SDK が生成したタグ。同じデバイスでホストされているアプリの関連付けに役立ちます。 あらゆる状況でのアプリの関連付けを保証するものではありません。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|
|deviceName|String|ホスト デバイスの名前 ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|flaggedReasons|String コレクション|アプリ登録にフラグが設定された、0 個以上の理由。 例: ルートのデバイス上で実行されているアプリ ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|userId|String|このアプリの登録が属するユーザー ID。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|
|appIdentifier|[mobileAppIdentifier](../resources/intune_mam_mobileappidentifier.md)|アプリ パッケージの識別子 ([managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承)|
|id|String|エンティティのキー。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|
|version|String|エンティティのバージョン。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|appliedPolicies|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) コレクション|登録済みのアプリが管理サービスと最後に同期したときに、すでに適用されていた 0 個以上のポリシーです。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|
|intendedPolicies|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) コレクション|現時点で、管理者がアプリに対して意図した 0 個以上のポリシーです。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|
|operations|[managedAppOperation](../resources/intune_mam_managedappoperation.md) コレクション|アプリ登録でトリガーされた、0 個以上の長時間実行の操作です。 [managedAppRegistration](../resources/intune_mam_managedappregistration.md) から継承します|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosManagedAppRegistration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosManagedAppRegistration",
  "createdDateTime": "String (timestamp)",
  "lastSyncDateTime": "String (timestamp)",
  "applicationVersion": "String",
  "managementSdkVersion": "String",
  "platformVersion": "String",
  "deviceType": "String",
  "deviceTag": "String",
  "deviceName": "String",
  "flaggedReasons": [
    "String"
  ],
  "userId": "String",
  "appIdentifier": {
    "@odata.type": "microsoft.graph.iosMobileAppIdentifier",
    "bundleId": "String"
  },
  "id": "String (identifier)",
  "version": "String"
}
```



