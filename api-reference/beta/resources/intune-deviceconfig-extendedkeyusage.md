---
title: extendedKeyUsage リソースの種類
description: カスタム拡張キー使用法の定義
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: d02154b9513e1ef3edac8cf823bd718d3e356691
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36325583"
---
# <a name="extendedkeyusage-resource-type"></a>extendedKeyUsage リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

カスタム拡張キー使用法の定義

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|name|String|拡張キー使用法の名前|
|objectIdentifier|String|拡張キー使用法のオブジェクト識別子|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.extendedKeyUsage"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.extendedKeyUsage",
  "name": "String",
  "objectIdentifier": "String"
}
```



