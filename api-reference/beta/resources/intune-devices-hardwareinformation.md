---
title: hardwareInformation リソースの種類
description: 特定のデバイスのハードウェア情報です。
ms.openlocfilehash: 90762426ef3d7b550b9a6fe89343e54d797b3a51
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27070883"
---
# <a name="hardwareinformation-resource-type"></a>hardwareInformation リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

特定のデバイスのハードウェア情報です。
## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|シリアル番号|String|シリアル番号です。|
|totalStorageSpace|Int64|デバイスの合計容量。|
|freeStorageSpace|Int64|デバイスの空き容量。|
|imei|String|IMEI|
|meid|String|MEID|
|manufacturer|String|デバイスのメーカー|
|model|String|デバイスのモデル|
|phoneNumber|String|デバイスの電話番号|
|subscriberCarrier|String|デバイスのサブスクライバーのキャリア|
|cellularTechnology|String|デバイスの携帯電話のテクノロジー|
|wifiMac|String|デバイスの WiFi の MAC アドレス|
|operatingSystemLanguage|String|デバイスのオペレーティング システムの言語|
|isSupervised|Boolean|デバイスのコールを管理モード|
|isEncrypted|Boolean|デバイスの暗号化の状態|
|isSharedDevice|ブール値|IPad の共有|
|sharedDeviceCachedUsers|[sharedAppleDeviceUser](../resources/intune-devices-sharedappledeviceuser.md)コレクション|共有の Apple デバイス上のすべてのユーザー|
|tpmSpecificationVersion|String|仕様のバージョンを指定する文字列。|
|operatingSystemEdition|String|OS のエディションを指定する文字列。|
|deviceFullQualifiedDomainName|String|(存在する場合) は、デバイスの完全修飾ドメイン名を返します。 デバイスがドメインに参加していない場合は、空の文字列を返します。 |
|deviceGuardVirtualizationBasedSecurityHardwareRequirementState|[deviceGuardVirtualizationBasedSecurityHardwareRequirementState](../resources/intune-devices-deviceguardvirtualizationbasedsecurityhardwarerequirementstate.md)|仮想化ベースのセキュリティ ハードウェアの要件の状態です。 可能な値は、`meetHardwareRequirements`、`secureBootRequired`、`dmaProtectionRequired`、`hyperVNotSupportedForGuestVM`、`hyperVNotAvailable` です。|
|deviceGuardVirtualizationBasedSecurityState|[deviceGuardVirtualizationBasedSecurityState](../resources/intune-devices-deviceguardvirtualizationbasedsecuritystate.md)|仮想化ベースのセキュリティの状態です。 . 可能な値は、`running`、`rebootRequired`、`require64BitArchitecture`、`notLicensed`、`notConfigured`、`doesNotMeetHardwareRequirements`、`other` です。|
|deviceGuardLocalSystemAuthorityCredentialGuardState|[deviceGuardLocalSystemAuthorityCredentialGuardState](../resources/intune-devices-deviceguardlocalsystemauthoritycredentialguardstate.md)|ローカル システム機関 (LSA) の資格情報のガード状態です。 . 可能な値は、`running`、`rebootRequired`、`notLicensed`、`notConfigured`、`virtualizationBasedSecurityNotRunning` です。|

## <a name="relationships"></a>リレーションシップ
なし
## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.hardwareInformation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.hardwareInformation",
  "serialNumber": "String",
  "totalStorageSpace": 1024,
  "freeStorageSpace": 1024,
  "imei": "String",
  "meid": "String",
  "manufacturer": "String",
  "model": "String",
  "phoneNumber": "String",
  "subscriberCarrier": "String",
  "cellularTechnology": "String",
  "wifiMac": "String",
  "operatingSystemLanguage": "String",
  "isSupervised": true,
  "isEncrypted": true,
  "isSharedDevice": true,
  "sharedDeviceCachedUsers": [
    {
      "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
      "userPrincipalName": "String",
      "dataToSync": true,
      "dataQuota": 1024,
      "dataUsed": 1024
    }
  ],
  "tpmSpecificationVersion": "String",
  "operatingSystemEdition": "String",
  "deviceFullQualifiedDomainName": "String",
  "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "String",
  "deviceGuardVirtualizationBasedSecurityState": "String",
  "deviceGuardLocalSystemAuthorityCredentialGuardState": "String"
}
```




