# <a name="mobileappcontentfile-resource-type"></a>mobileAppContentFile リソース タイプ

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

特定の mobileAppContent バージョンに関連付けられている単一のインストーラー ファイルのプロパティが含まれています。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List mobileAppContentFiles](../api/intune_apps_mobileappcontentfile_list.md)|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) コレクション|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get mobileAppContentFile](../api/intune_apps_mobileappcontentfile_get.md)|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md)|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create mobileAppContentFile](../api/intune_apps_mobileappcontentfile_create.md)|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md)|新しい [mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) オブジェクトを作成します。|
|[Delete mobileAppContentFile](../api/intune_apps_mobileappcontentfile_delete.md)|なし|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) を削除します。|
|[Update mobileAppContentFile](../api/intune_apps_mobileappcontentfile_update.md)|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md)|[mobileAppContentFile](../resources/intune_apps_mobileappcontentfile.md) オブジェクトのプロパティを更新します。|
|[commit action](../api/intune_apps_mobileappcontentfile_commit.md)|なし|特定のアプリのファイルをコミットします。|
|[renewUpload action](../api/intune_apps_mobileappcontentfile_renewupload.md)|なし|アプリケーション ファイルのアップロード用の SAS URI を更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|azureStorageUri|String|Azure ストレージ URI。|
|isCommitted|Boolean|ファイルがコミットされたかどうかを示す値。|
|id|String|ファイル ID。|
|createdDateTime|DateTimeOffset|ファイルが作成された時刻。|
|name|String|ファイル名。|
|size|Int64|暗号化する前のファイルのサイズ。|
|sizeEncrypted|Int64|暗号化した後のファイルのサイズ。|
|azureStorageUriExpirationDateTime|DateTimeOffset|Azure ストレージ URI の有効期限が切れる時刻。|
|manifest|Binary|マニフェスト情報。|
|uploadState|String|現在のアップロード要求の状態。 可能な値は、`success`、`transientError`、`error`、`unknown`、`azureStorageUriRequestSuccess`、`azureStorageUriRequestPending`、`azureStorageUriRequestFailed`、`azureStorageUriRequestTimedOut`、`azureStorageUriRenewalSuccess`、`azureStorageUriRenewalPending`、`azureStorageUriRenewalFailed`、`azureStorageUriRenewalTimedOut`、`commitFileSuccess`、`commitFilePending`、`commitFileFailed`、`commitFileTimedOut` です。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppContentFile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppContentFile",
  "azureStorageUri": "String",
  "isCommitted": true,
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "name": "String",
  "size": 1024,
  "sizeEncrypted": 1024,
  "azureStorageUriExpirationDateTime": "String (timestamp)",
  "manifest": "binary",
  "uploadState": "String"
}
```



