---
title: deliveryOptimizationBandwidthPercentage リソースの種類
description: 割合として指定された帯域幅制限。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 782ed9a68ee3e759e719b14c2241cc1a02e30138
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36333353"
---
# <a name="deliveryoptimizationbandwidthpercentage-resource-type"></a>deliveryOptimizationBandwidthPercentage リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

割合として指定された帯域幅制限。


[DeliveryOptimizationBandwidth](../resources/intune-deviceconfig-deliveryoptimizationbandwidth.md)から継承します。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|maximumBackgroundBandwidthPercentage|Int32|利用可能なダウンロード帯域幅 (0-100) の割合として、配信の最適化で使用される最大バックグラウンドダウンロード帯域幅を指定します。 有効な値は 0 から 100 までです
既定値の 0 (ゼロ) は、配信の最適化が、バックグラウンドダウンロードに使用可能な帯域幅を使用するように動的に調整されることを意味します。 有効な値は 0 から 100 までです|
|maximumForegroundBandwidthPercentage|Int32|利用可能なダウンロード帯域幅 (0-100) の割合として、すべての同時ダウンロードアクティビティにおいて配信の最適化で使用されるフォアグラウンドの最大ダウンロード帯域幅を指定します。 有効な値は 0 から 100 までです
既定値の 0 (ゼロ) は、配信の最適化が、フォアグラウンドダウンロードに使用可能な帯域幅を使用するように動的に調整されることを意味します。 有効な値は 0 から 100 までです|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deliveryOptimizationBandwidthPercentage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deliveryOptimizationBandwidthPercentage",
  "maximumBackgroundBandwidthPercentage": 1024,
  "maximumForegroundBandwidthPercentage": 1024
}
```



