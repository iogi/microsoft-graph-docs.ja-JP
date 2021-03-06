# <a name="organization-resource-type"></a>organization リソースの種類

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

organization リソースは、グローバル設定インスタンスと、テナント レベルで操作およびプロビジョニングされるリソースを表わします。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List organizations](../api/intune_onboarding_organization_list.md)|[organization](../resources/intune_onboarding_organization.md) コレクション|[organization](../resources/intune_onboarding_organization.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get organization](../api/intune_onboarding_organization_get.md)|[organization](../resources/intune_onboarding_organization.md)|[organization](../resources/intune_onboarding_organization.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Update organization](../api/intune_onboarding_organization_update.md)|[organization](../resources/intune_onboarding_organization.md)|[organization](../resources/intune_onboarding_organization.md) オブジェクトのプロパティを更新します。|
|[setMobileDeviceManagementAuthority アクション](../api/intune_onboarding_organization_setmobiledevicemanagementauthority.md)|Int32|モバイル デバイス管理権限の設定|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列型 (String)|オブジェクトの GUID。|
|mobileDeviceManagementAuthority|文字列型 (String)|モバイル デバイス管理権限。 可能な値: `unknown`、`intune`、`sccm`、`office365`。|

## <a name="relationships"></a>関係
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.organization"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.organization",
  "id": "String (identifier)",
  "mobileDeviceManagementAuthority": "String"
}
```



