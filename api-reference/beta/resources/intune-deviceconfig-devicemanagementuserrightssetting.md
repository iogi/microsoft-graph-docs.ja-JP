---
title: deviceManagementUserRightsSetting リソースの種類
description: ユーザー権限の設定を表します。
ms.openlocfilehash: e657c15a76700ef87283220254937ec685c57784
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27071693"
---
# <a name="devicemanagementuserrightssetting-resource-type"></a>deviceManagementUserRightsSetting リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

ユーザー権限の設定を表します。
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|state|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|このユーザーの現在の状態を表す権限を設定します。 可能な値は、`notConfigured`、`blocked`、`allowed` です。|
|localUsersOrGroups|[deviceManagementUserRightsLocalUserOrGroup](../resources/intune-deviceconfig-devicemanagementuserrightslocaluserorgroup.md)コレクション|ローカル ユーザーまたはグループはこの設定の状態が許可されている場合に、デバイスの設定のコレクションを表します。 このコレクションには、最大で 500 個の要素を含めることができます。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceManagementUserRightsSetting"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementUserRightsSetting",
  "state": "String",
  "localUsersOrGroups": [
    {
      "@odata.type": "microsoft.graph.deviceManagementUserRightsLocalUserOrGroup",
      "name": "String",
      "description": "String",
      "securityIdentifier": "String"
    }
  ]
}
```




