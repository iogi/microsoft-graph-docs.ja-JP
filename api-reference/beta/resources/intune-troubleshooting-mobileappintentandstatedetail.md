---
title: mobileAppIntentAndStateDetail リソースの種類
description: モバイル アプリケーションの目的および特定のデバイスのインストールの状態です。
ms.openlocfilehash: d793f23346991c681ecfd4e0d55272153496ae36
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27066294"
---
# <a name="mobileappintentandstatedetail-resource-type"></a>mobileAppIntentAndStateDetail リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

モバイル アプリケーションの目的および特定のデバイスのインストールの状態です。
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|applicationId|文字列型 (String)|MobieApp の識別子です。|
|displayName|String|管理者が提供またはインポートしたアプリのタイトル。|
|mobileAppIntent|[mobileAppIntent](../resources/intune-troubleshooting-mobileappintent.md)|モバイル アプリケーションの目的です。 可能な値は、`available`、`notAvailable`、`requiredInstall`、`requiredUninstall`、`requiredAndAvailableInstall`、`availableInstallWithoutEnrollment`、`exclude` です。|
|displayVersion|String|人間の読み取り可能なバージョンのアプリケーション|
|installState|[resultantAppState](../resources/intune-shared-resultantappstate.md)|アプリケーションのインストール状態です。 可能な値は、`installed`、`failed`、`notInstalled`、`uninstallFailed`、`pendingInstall`、`unknown`、`notApplicable` です。|
|supportedDeviceTypes|[mobileAppSupportedDeviceType](../resources/intune-troubleshooting-mobileappsupporteddevicetype.md)コレクション|アプリケーションのサポートされているプラットフォームです。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppIntentAndStateDetail"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppIntentAndStateDetail",
  "applicationId": "String",
  "displayName": "String",
  "mobileAppIntent": "String",
  "displayVersion": "String",
  "installState": "String",
  "supportedDeviceTypes": [
    {
      "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType",
      "type": "String",
      "minimumOperatingSystemVersion": "String",
      "maximumOperatingSystemVersion": "String"
    }
  ]
}
```




