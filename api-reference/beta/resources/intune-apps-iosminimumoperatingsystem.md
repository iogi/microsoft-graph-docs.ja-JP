---
title: iosMinimumOperatingSystem リソースの種類
description: iOS モバイル アプリに必要な最小限のオペレーティング システムのプロパティが含まれます。
ms.openlocfilehash: 686128d3412b63e5441adfd1ccf62d5fc7c23ab6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27066938"
---
# <a name="iosminimumoperatingsystem-resource-type"></a>iosMinimumOperatingSystem リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

iOS モバイル アプリに必要な最小限のオペレーティング システムのプロパティが含まれます。
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|v8_0|ブール型 (Boolean)|バージョン 8.0 以降。|
|v9_0|ブール型 (Boolean)|バージョン 9.0 以降。|
|v10_0|ブール型 (Boolean)|バージョン 10.0 以降。|
|v11_0|ブール型 (Boolean)|バージョン 11.0 以降。|
|v12_0|ブール値|12.0 またはそれ以降のバージョンです。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMinimumOperatingSystem",
  "v8_0": true,
  "v9_0": true,
  "v10_0": true,
  "v11_0": true,
  "v12_0": true
}
```




