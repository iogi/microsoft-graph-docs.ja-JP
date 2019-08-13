---
title: managedDeviceModelsAndManufacturers リソースの種類
description: アカウントの管理対象デバイスのモデルと製造 meatadata
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 1e9846b9d551b7ae226fe13c32100c8cbfd049ee
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36372266"
---
# <a name="manageddevicemodelsandmanufacturers-resource-type"></a>managedDeviceModelsAndManufacturers リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

アカウントの管理対象デバイスのモデルと製造 meatadata

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|deviceModels|文字列コレクション|アカウント内の管理されたデバイスのモデルの一覧|
|deviceManufacturers|文字列コレクション|アカウントで管理されているデバイスの製造元の一覧|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceModelsAndManufacturers"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceModelsAndManufacturers",
  "deviceModels": [
    "String"
  ],
  "deviceManufacturers": [
    "String"
  ]
}
```



