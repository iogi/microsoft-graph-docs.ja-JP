---
title: mobileAppRelationshipState リソースの種類
description: UPN とデバイス id のコンテキストでの子アプリのインストール状態の詳細について説明します。
author: tfitzmac
localization_priority: Normal
ms.prod: Intune
ms.openlocfilehash: e7f3dcbbc2544a4231cd5da102985d7142feb03a
ms.sourcegitcommit: 20fef447f7e658a454a3887ea49746142c22e45c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/11/2019
ms.locfileid: "31809278"
---
# <a name="mobileapprelationshipstate-resource-type"></a>mobileAppRelationshipState リソースの種類

> **重要:** ベータ版の Microsoft Graph api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

UPN とデバイス id のコンテキストでの子アプリのインストール状態の詳細について説明します。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|sourceIds|String コレクション|送信元モバイルアプリの id のコレクション。|
|targetId|文字列|関連するターゲットアプリの id。|
|targetdisplayname|文字列|関連するターゲットアプリの表示名。|
|deviceId|String|対応するデバイス id。|
|installState|[resultappstate](../resources/intune-shared-resultantappstate.md)|ターゲットアプリのアプリのインストール状態。 可能な値は、`installed`、`failed`、`notInstalled`、`uninstallFailed`、`pendingInstall`、`unknown`、`notApplicable` です。|
|installstatedetail|[resultantAppStateDetail](../resources/intune-apps-resultantappstatedetail.md)|アプリのインストール状態の詳細。 可能な値: `noAdditionalDetails`、 `dependencyFailedToInstall` `dependencyWithRequirementsNotMet` `dependencyPendingReboot` `dependencyWithAutoInstallDisabled` `seeInstallErrorCode` `autoInstallDisabled` `seeUninstallErrorCode` `pendingReboot` `installingDependencies` `powerShellScriptRequirementNotMet` `registryRequirementNotMet`、、、、、、、、、、、、 `fileSystemRequirementNotMet` `platformNotApplicable` `minimumCpuSpeedNotMet` `minimumLogicalProcessorCountNotMet` `minimumPhysicalMemoryNotMet` `minimumOsVersionNotMet` `minimumDiskSpaceNotMet`, `processorArchitectureNotApplicable`.|
|errorCode|Int32|ターゲットアプリのインストールまたはアンインストールに失敗した場合のエラーコード。|
|targetlastsyncdatetime|DateTimeOffset|ターゲットアプリの最終同期時刻。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppRelationshipState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppRelationshipState",
  "sourceIds": [
    "String"
  ],
  "targetId": "String",
  "targetDisplayName": "String",
  "deviceId": "String",
  "installState": "String",
  "installStateDetail": "String",
  "errorCode": 1024,
  "targetLastSyncDateTime": "String (timestamp)"
}
```




