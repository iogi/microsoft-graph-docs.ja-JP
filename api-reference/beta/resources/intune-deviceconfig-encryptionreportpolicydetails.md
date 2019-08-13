---
title: encryptionReportPolicyDetails リソースの種類
description: 暗号化レポートのポリシーの詳細
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 7271329a7536a6359bbc9662427e65e21ea39d8b
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36325611"
---
# <a name="encryptionreportpolicydetails-resource-type"></a>encryptionReportPolicyDetails リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

暗号化レポートのポリシーの詳細

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|policyId|String|暗号化レポートのポリシー Id|
|policyName|String|暗号化レポートのポリシー名|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.encryptionReportPolicyDetails"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.encryptionReportPolicyDetails",
  "policyId": "String",
  "policyName": "String"
}
```



