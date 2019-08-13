---
title: deliveryOptimizationBandwidthBusinessHoursLimit リソースの種類
description: 帯域幅の営業時間とパーセンテージの種類
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 533d4c0706f319f4b127f78af8340f215232e2b9
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36333388"
---
# <a name="deliveryoptimizationbandwidthbusinesshourslimit-resource-type"></a>deliveryOptimizationBandwidthBusinessHoursLimit リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

帯域幅の営業時間とパーセンテージの種類

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|bandwidthBeginBusinessHours|Int32|24時間形式 (0-23) を使用して営業時間の開始時刻を指定します。 有効な値は0から23までです|
|bandwidthEndBusinessHours|Int32|24時間形式 (0-23) を使用して営業時間の終了時刻を指定します。 有効な値は0から23までです|
|bandwidthPercentageDuringBusinessHours|Int32|営業時間内に制限する帯域幅の割合 (0-100) を指定します。 有効な値は 0 から 100 までです|
|bandwidthPercentageOutsideBusinessHours|Int32|勤務時間を制限する帯域幅の割合 (0-100) を指定します。 有効な値は 0 から 100 までです|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deliveryOptimizationBandwidthBusinessHoursLimit"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deliveryOptimizationBandwidthBusinessHoursLimit",
  "bandwidthBeginBusinessHours": 1024,
  "bandwidthEndBusinessHours": 1024,
  "bandwidthPercentageDuringBusinessHours": 1024,
  "bandwidthPercentageOutsideBusinessHours": 1024
}
```



