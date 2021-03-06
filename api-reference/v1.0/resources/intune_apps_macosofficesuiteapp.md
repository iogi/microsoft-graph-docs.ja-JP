# <a name="macosofficesuiteapp-resource-type"></a>macOSOfficeSuiteApp リソース タイプ

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

macOS Office スイート アプリのプロパティと継承されるプロパティを含みます。

[mobileApp](../resources/intune_apps_mobileapp.md) から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List macOSOfficeSuiteApps](../api/intune_apps_macosofficesuiteapp_list.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) コレクション|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_get.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_create.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|新しい [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトを作成します。|
|[Delete macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_delete.md)|なし|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) を削除します。|
|[Update macOSOfficeSuiteApp](../api/intune_apps_macosofficesuiteapp_update.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md)|[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトのプロパティを更新します。|

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

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|categories|[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) コレクション|このアプリのカテゴリのリスト。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|
|assignments|[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) コレクション|このモバイル アプリのグループ割り当てのリスト。 [mobileApp](../resources/intune_apps_mobileapp.md) から継承します|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.macOSOfficeSuiteApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
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
  "publishingState": "String"
}
```



