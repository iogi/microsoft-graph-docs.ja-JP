---
title: softwareUpdateStatusSummary リソースの種類
description: まだ文書化されていません
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 90a73cb39bfb0f5975434048427a4d761d47d99c
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36367912"
---
# <a name="softwareupdatestatussummary-resource-type"></a>softwareUpdateStatusSummary リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

まだ文書化されていません

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[Get softwareUpdateStatusSummary](../api/intune-deviceconfig-softwareupdatestatussummary-get.md)|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md)|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Update softwareUpdateStatusSummary](../api/intune-deviceconfig-softwareupdatestatussummary-update.md)|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md)|[softwareUpdateStatusSummary](../resources/intune-deviceconfig-softwareupdatestatussummary.md) オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。|
|displayName|String|ポリシーの名前。|
|compliantDeviceCount|Int32|準拠デバイスの数。|
|nonCompliantDeviceCount|Int32|準拠していないデバイスの数。|
|remediatedDeviceCount|Int32|修復済みデバイスの数。|
|errorDeviceCount|Int32|エラーが発生したデバイスの数。|
|unknownDeviceCount|Int32|不明なデバイスの数。|
|conflictDeviceCount|Int32|競合デバイスの数。|
|notApplicableDeviceCount|Int32|該当しないデバイスの数。|
|compliantUserCount|Int32|準拠ユーザーの数。|
|nonCompliantUserCount|Int32|準拠していないユーザーの数。|
|remediatedUserCount|Int32|修復済みユーザーの数。|
|errorUserCount|Int32|エラーが発生したユーザーの数。|
|unknownUserCount|Int32|不明なユーザーの数。|
|conflictUserCount|Int32|競合ユーザーの数。|
|notApplicableUserCount|Int32|該当しないユーザーの数。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.softwareUpdateStatusSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.softwareUpdateStatusSummary",
  "id": "String (identifier)",
  "displayName": "String",
  "compliantDeviceCount": 1024,
  "nonCompliantDeviceCount": 1024,
  "remediatedDeviceCount": 1024,
  "errorDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "conflictDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "compliantUserCount": 1024,
  "nonCompliantUserCount": 1024,
  "remediatedUserCount": 1024,
  "errorUserCount": 1024,
  "unknownUserCount": 1024,
  "conflictUserCount": 1024,
  "notApplicableUserCount": 1024
}
```



