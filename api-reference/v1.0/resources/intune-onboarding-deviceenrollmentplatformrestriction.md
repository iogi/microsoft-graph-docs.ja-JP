---
title: deviceEnrollmentPlatformRestriction リソースの種類
description: プラットフォーム固有の登録の制限
ms.openlocfilehash: b6d4ea3acf4995548fce7f2c86b3c95c444b59b5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27024235"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a>deviceEnrollmentPlatformRestriction リソースの種類

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

プラットフォーム固有の登録の制限
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|platformBlocked|ブール型 (Boolean)|登録で対象プラットフォームをブロックします|
|personalDeviceEnrollmentBlocked|ブール型 (Boolean)|個人所有のデバイスの登録をブロックします|
|osMinimumVersion|文字列型 (String)|サポートされる最小 OS バージョン|
|osMaximumVersion|文字列型 (String)|サポートされる最大 OS バージョン|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestriction",
  "platformBlocked": true,
  "personalDeviceEnrollmentBlocked": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String"
}
```


