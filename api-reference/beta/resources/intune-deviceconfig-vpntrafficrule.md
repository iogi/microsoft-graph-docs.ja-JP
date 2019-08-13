---
title: vpnTrafficRule リソースの種類
description: VPN トラフィックルールの定義。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 399c0e57a4e7bf29fc1772d8178ebd9510a85e9c
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36367562"
---
# <a name="vpntrafficrule-resource-type"></a>vpnTrafficRule リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

VPN トラフィックルールの定義。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|name|String|拡張子.|
|プロトコル|Int32|プロトコル (0-255)。 有効な値は 0 ~ 255|
|localPortRanges|[numberRange](../resources/intune-deviceconfig-numberrange.md)コレクション|プロトコルが TCP または UDP (6 または 17) の場合にのみ、ローカルポート範囲を設定できます。 このコレクションには、最大で 500 個の要素を含めることができます。|
|remotePortRanges|[numberRange](../resources/intune-deviceconfig-numberrange.md)コレクション|プロトコルが TCP または UDP (6 または 17) の場合にのみ、リモートポート範囲を設定できます。 このコレクションには、最大で 500 個の要素を含めることができます。|
|localAddressRanges|[iPv4Range](../resources/intune-shared-ipv4range.md)コレクション|ローカルアドレス範囲。 このコレクションには、最大で 500 個の要素を含めることができます。|
|remoteAddressRanges|[iPv4Range](../resources/intune-shared-ipv4range.md)コレクション|リモートアドレス範囲。 このコレクションには、最大で 500 個の要素を含めることができます。|
|appId|String|アプリ識別子。このトラフィックルールがアプリによってトリガーされた場合。|
|appType|[vpnTrafficRuleAppType](../resources/intune-deviceconfig-vpntrafficruleapptype.md)|アプリの種類。このトラフィックルールがアプリによってトリガーされた場合。 可能な値は、`none`、`desktop`、`universal` です。|
|routingPolicyType|[vpnTrafficRuleRoutingPolicyType](../resources/intune-deviceconfig-vpntrafficruleroutingpolicytype.md)|アプリがトリガーされたときに、このルートに沿った分割トンネリングを有効にするかどうかを示します。 可能な値は、`none`、`splitTunnel`、`forceTunnel` です。|
|差出人|String|このトラフィック規則に関連付けられているクレーム。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnTrafficRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnTrafficRule",
  "name": "String",
  "protocols": 1024,
  "localPortRanges": [
    {
      "@odata.type": "microsoft.graph.numberRange",
      "lowerNumber": 1024,
      "upperNumber": 1024
    }
  ],
  "remotePortRanges": [
    {
      "@odata.type": "microsoft.graph.numberRange",
      "lowerNumber": 1024,
      "upperNumber": 1024
    }
  ],
  "localAddressRanges": [
    {
      "@odata.type": "microsoft.graph.iPv4Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "remoteAddressRanges": [
    {
      "@odata.type": "microsoft.graph.iPv4Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "appId": "String",
  "appType": "String",
  "routingPolicyType": "String",
  "claims": "String"
}
```



