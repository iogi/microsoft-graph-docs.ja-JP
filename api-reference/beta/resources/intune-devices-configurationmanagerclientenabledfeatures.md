---
title: configurationManagerClientEnabledFeatures リソースの種類
description: 構成マネージャーのクライアントに対応した機能
ms.openlocfilehash: 60d0e9e78bc4b641bb1f9ee0d61cc09744500424
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067839"
---
# <a name="configurationmanagerclientenabledfeatures-resource-type"></a>configurationManagerClientEnabledFeatures リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

構成マネージャーのクライアントに対応した機能
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|inventory|Boolean|在庫が Intune によって管理されているかどうか|
|modernApps|Boolean|モダン アプリケーションが Intune によって管理されているかどうか|
|resourceAccess|Boolean|リソース アクセスが Intune によって管理されているかどうか|
|deviceConfiguration|Boolean|デバイス構成が Intune によって管理されているかどうか|
|compliancePolicy|Boolean|コンプライアンス ポリシーが Intune によって管理されているかどうか|
|windowsUpdateForBusiness|Boolean|Windows Update for Business が Intune によって管理されているかどうか|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerClientEnabledFeatures",
  "inventory": true,
  "modernApps": true,
  "resourceAccess": true,
  "deviceConfiguration": true,
  "compliancePolicy": true,
  "windowsUpdateForBusiness": true
}
```




