---
title: importedWindowsAutopilotDeviceIdentityState リソースの種類
description: まだ文書化されていません
ms.openlocfilehash: cdb13df520d109ddcc49e2637652499186ac9f24
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27071312"
---
# <a name="importedwindowsautopilotdeviceidentitystate-resource-type"></a>importedWindowsAutopilotDeviceIdentityState リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

まだ文書化されていません
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|deviceImportStatus|[importedWindowsAutopilotDeviceIdentityImportStatus](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityimportstatus.md)|Device Directory Service (DDS) から報告されたデバイスの状態です。 可能な値は、`unknown`、`pending`、`partial`、`complete`、`error` です。|
|deviceRegistrationId|String|正常に追加されたと Devce Directory Service (DDS) から報告されたデバイスの Devce Registration ID です。|
|deviceErrorCode|Int32|Device Directory Service (DDS) から報告されたデバイス エラー コードです。|
|deviceErrorName|String|Device Directory Service (DDS) から報告されたデバイス エラー名です。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
  "deviceImportStatus": "String",
  "deviceRegistrationId": "String",
  "deviceErrorCode": 1024,
  "deviceErrorName": "String"
}
```




