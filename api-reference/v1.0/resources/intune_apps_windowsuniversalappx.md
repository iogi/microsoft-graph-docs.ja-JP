# <a name="windowsuniversalappx-resource-type"></a>windowsUniversalAppX リソース タイプ

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

Windows ユニバーサル AppX 基幹業務アプリのプロパティと継承されたプロパティが含まれます。

[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List windowsUniversalAppXs](../api/intune_apps_windowsuniversalappx_list.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) コレクション|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_get.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_create.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|新しい [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) オブジェクトを作成します。|
|[Delete windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_delete.md)|なし|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) を削除します。|
|[Update windowsUniversalAppX](../api/intune_apps_windowsuniversalappx_update.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md)|[windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|displayName|String|管理者が提供またはインポートしたアプリのタイトル。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|description|String|アプリの説明。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|publisher|String|アプリの発行元です。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|largeIcon|[mimeContent](../resources/intune_apps_mimecontent.md)|アプリの詳細に表示され、アイコンのアップロードに使用される大きいアイコン。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|createdDateTime|DateTimeOffset|アプリが作成された日時。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|アプリが最後に変更された日時。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|isFeatured|Boolean|アプリが管理者のおすすめとしてマークされたかどうかを示す値。[mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|privacyInformationUrl|String|プライバシーに関する声明の URL。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|informationUrl|String|詳細情報の URL。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|owner|String|アプリの所有者。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|developer|String|アプリの開発者。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|notes|String|アプリ用のメモ。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|publishingState|String|アプリの発行の状態。 アプリが発行されていない限り、アプリを割り当てることができません。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します。可能な値は、`notPublished`、`processing`、`published` です。|
|committedContentVersion|String|内部にコミットされたコンテンツのバージョン。 [mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します|
|fileName|String|メインの LOB アプリケーションのファイル名。 [mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します|
|size|Int64|アップロードされたすべてのファイルを含む合計サイズ。 [mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します|
|applicableArchitectures|String|このアプリを実行できる Windows アーキテクチャ。 可能な値は、`none`、`x86`、`x64`、`arm`、`neutral` です。|
|applicableDeviceTypes|String|このアプリを実行できる Windows デバイスの種類。 可能な値は、`none`、`desktop`、`mobile`、`holographic`、`team` です。|
|identityName|String|ID 名。|
|identityPublisherHash|String|ID の発行元のハッシュ。|
|identityResourceIdentifier|String|ID のリソースの識別子。|
|isBundle|Boolean|アプリがバンドルかどうかを示します。|
|minimumSupportedOperatingSystem|[windowsMinimumOperatingSystem](../resources/intune_apps_windowsminimumoperatingsystem.md)|該当するオペレーティング システムの最小の値です。|
|identityVersion|String|ID のバージョン。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|categories|[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) コレクション|このアプリのカテゴリのリスト。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|assignments|[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) コレクション|このモバイル アプリのグループ割り当てのリスト。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|contentVersions|[mobileAppContent](../resources/intune_apps_mobileappcontent.md) コレクション|このアプリのコンテンツのバージョンのリスト。 [mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsUniversalAppX"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "publishingState": "String",
  "committedContentVersion": "String",
  "fileName": "String",
  "size": 1024,
  "applicableArchitectures": "String",
  "applicableDeviceTypes": "String",
  "identityName": "String",
  "identityPublisherHash": "String",
  "identityResourceIdentifier": "String",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "String"
}
```



