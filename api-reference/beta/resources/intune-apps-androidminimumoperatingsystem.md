---
title: androidMinimumOperatingSystem リソースの種類
description: Android モバイル アプリに必要な最小限のオペレーティング システムのプロパティが含まれます。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: bc1bfa8f0bed261b79a1cae87cd1db64e8a099c4
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36366904"
---
# <a name="androidminimumoperatingsystem-resource-type"></a>androidMinimumOperatingSystem リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Android モバイル アプリに必要な最小限のオペレーティング システムのプロパティが含まれます。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|v4_0|Boolean|バージョン 4.0 以降。|
|v4_0_3|Boolean|バージョン 4.0.3 以降。|
|v4_1|Boolean|バージョン 4.1 以降。|
|v4_2|Boolean|バージョン 4.2 以降。|
|v4_3|Boolean|バージョン 4.3 以降。|
|v4_4|Boolean|バージョン 4.4 以降。|
|v5_0|Boolean|バージョン 5.0 以降。|
|v5_1|Boolean|バージョン 5.1 以降。|
|v6_0|Boolean|バージョン6.0 以降。|
|v7_0|Boolean|バージョン7.0 以降。|
|v7_1|Boolean|バージョン7.1 以降。|
|v8_0|Boolean|バージョン 8.0 以降。|
|v8_1|ブール型 (Boolean)|バージョン8.1 以降。|
|v9_0|ブール型 (Boolean)|バージョン 9.0 以降。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.androidMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidMinimumOperatingSystem",
  "v4_0": true,
  "v4_0_3": true,
  "v4_1": true,
  "v4_2": true,
  "v4_3": true,
  "v4_4": true,
  "v5_0": true,
  "v5_1": true,
  "v6_0": true,
  "v7_0": true,
  "v7_1": true,
  "v8_0": true,
  "v8_1": true,
  "v9_0": true
}
```



