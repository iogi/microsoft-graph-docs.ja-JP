---
title: windowsDefenderScanActionResult リソースの種類
description: Windows Defender の最後のスキャン結果
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 24cb44c634706b51baef2e840dc17e5622972233
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36366505"
---
# <a name="windowsdefenderscanactionresult-resource-type"></a>windowsDefenderScanActionResult リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Windows Defender の最後のスキャン結果


[deviceActionResult](../resources/intune-devices-deviceactionresult.md) からの継承

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|actionName|String|[deviceActionResult](../resources/intune-devices-deviceactionresult.md) から継承されるアクション名|
|actionState|[actionState](../resources/intune-shared-actionstate.md)|[Deviceactionresult](../resources/intune-devices-deviceactionresult.md)から継承されるアクションの状態。 可能な値は、`none`、`pending`、`canceled`、`active`、`done`、`failed`、`notSupported` です。|
|startDateTime|DateTimeOffset|アクションが開始された時刻。[deviceActionResult](../resources/intune-devices-deviceactionresult.md) から継承。|
|lastUpdatedDateTime|DateTimeOffset|アクション状態の最終更新時刻。[deviceActionResult](../resources/intune-devices-deviceactionresult.md) から継承|
|scanType|文字列型 (String)|スキャンの種類。フル スキャンまたはクイック スキャン|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsDefenderScanActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsDefenderScanActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "scanType": "String"
}
```



