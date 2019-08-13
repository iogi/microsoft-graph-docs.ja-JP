---
title: deviceConfigurationUserStatus リソースの種類
description: まだ文書化されていません
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: c01e9b3ec10ac032ee8eca41d92e36eca35d67c5
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36332891"
---
# <a name="deviceconfigurationuserstatus-resource-type"></a>deviceConfigurationUserStatus リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

まだ文書化されていません

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[deviceConfigurationUserStatuses のリスト](../api/intune-deviceconfig-deviceconfigurationuserstatus-list.md)|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) コレクション|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[deviceConfigurationUserStatus の取得](../api/intune-deviceconfig-deviceconfigurationuserstatus-get.md)|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[deviceConfigurationUserStatus の作成](../api/intune-deviceconfig-deviceconfigurationuserstatus-create.md)|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|新しい [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) オブジェクトを作成します。|
|[deviceConfigurationUserStatus の削除](../api/intune-deviceconfig-deviceconfigurationuserstatus-delete.md)|なし|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) を削除します。|
|[deviceConfigurationUserStatus の更新](../api/intune-deviceconfig-deviceconfigurationuserstatus-update.md)|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。|
|userDisplayName|String|DevicePolicyStatus のユーザー名。|
|devicesCount|Int32|そのユーザーのデバイスの数。|
|status|[complianceStatus](../resources/intune-shared-compliancestatus.md)|ポリシー レポートのコンプライアンスの状態。 可能な値は、`unknown`、`notApplicable`、`compliant`、`remediated`、`nonCompliant`、`error`、`conflict`、`notAssigned` です。|
|lastReportedDateTime|DateTimeOffset|ポリシー レポートの最終変更日時。|
|userPrincipalName|String|UserPrincipalName。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationUserStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
  "id": "String (identifier)",
  "userDisplayName": "String",
  "devicesCount": 1024,
  "status": "String",
  "lastReportedDateTime": "String (timestamp)",
  "userPrincipalName": "String"
}
```



