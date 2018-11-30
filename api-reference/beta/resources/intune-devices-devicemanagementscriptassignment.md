---
title: deviceManagementScriptAssignment リソースの種類
description: デバイス管理のスクリプトをグループに割り当てるために使用するプロパティが含まれています。
ms.openlocfilehash: fb4be06fe36153cd9a015808823cf1e90d86a707
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27073985"
---
# <a name="devicemanagementscriptassignment-resource-type"></a>deviceManagementScriptAssignment リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

デバイス管理のスクリプトをグループに割り当てるために使用するプロパティが含まれています。
## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[リスト deviceManagementScriptAssignments](../api/intune-devices-devicemanagementscriptassignment-list.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)コレクション|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトのプロパティと関係を一覧表示します。|
|[DeviceManagementScriptAssignment を取得します。](../api/intune-devices-devicemanagementscriptassignment-get.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトのプロパティと関係を参照してください。|
|[DeviceManagementScriptAssignment を作成します。](../api/intune-devices-devicemanagementscriptassignment-create.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|新しい[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトを作成します。|
|[DeviceManagementScriptAssignment を削除します。](../api/intune-devices-devicemanagementscriptassignment-delete.md)|なし|の[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)を削除します。|
|[DeviceManagementScriptAssignment を更新します。](../api/intune-devices-devicemanagementscriptassignment-update.md)|[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)|[DeviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|デバイス管理スクリプトのグループの割り当てエンティティのキーです。|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|Azure Active Directory グループの Id は、対象としてスクリプトをします。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```




