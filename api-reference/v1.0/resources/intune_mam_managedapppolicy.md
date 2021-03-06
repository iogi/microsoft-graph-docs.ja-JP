# <a name="managedapppolicy-resource-type"></a>managedAppPolicy リソースの種類

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

ManagedAppPolicy リソースは、プラットフォーム特有のポリシーの基本型を表します。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List managedAppPolicies](../api/intune_mam_managedapppolicy_list.md)|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) コレクション|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get managedAppPolicy](../api/intune_mam_managedapppolicy_get.md)|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md)|[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[targetApps アクション](../api/intune_mam_managedapppolicy_targetapps.md)|なし|まだ文書化されていません|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|displayName|文字列型 (String)|ポリシーの表示名。|
|description|文字列型 (String)|ポリシーの説明。|
|createdDateTime|DateTimeOffset|ポリシーが作成された日時。|
|lastModifiedDateTime|DateTimeOffset|ポリシーが変更された最終日時。|
|id|文字列型 (String)|エンティティのキー。|
|version|文字列型 (String)|エンティティのバージョン。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedAppPolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedAppPolicy",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "version": "String"
}
```



