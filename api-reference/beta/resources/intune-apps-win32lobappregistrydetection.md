---
title: win32LobAppRegistryDetection リソースの種類
description: Win32 アプリを検出するためのレジストリプロパティが含まれています
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 0fbd54fe4ed8f7df35ae6acdcde8722b98d1c24a
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36335551"
---
# <a name="win32lobappregistrydetection-resource-type"></a>win32LobAppRegistryDetection リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

Win32 アプリを検出するためのレジストリプロパティが含まれています


[Win32LobAppDetection](../resources/intune-apps-win32lobappdetection.md)から継承します。

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|check32BitOn64System|Boolean|このレジストリパスが、64ビットシステムの32ビットアプリをチェックするためのものであるかどうかを示す値。|
|キーパス|String|Win32 基幹業務 (LoB) アプリを検出するためのレジストリキーのパス|
|valueName|String|レジストリ値の名前|
|detectionType|[win32LobAppRegistryDetectionType](../resources/intune-apps-win32lobappregistrydetectiontype.md)|レジストリデータ検出の種類。 使用可能な値: `notConfigured`、`exists`、`doesNotExist`、`string`、`integer`、`version`。|
|operator|[win32LobAppDetectionOperator](../resources/intune-apps-win32lobappdetectionoperator.md)|レジストリデータを検出するための演算子。 可能な値は、`notConfigured`、`equal`、`notEqual`、`greaterThan`、`greaterThanOrEqual`、`lessThan`、`lessThanOrEqual` です。|
|detectionValue|String|レジストリの検出値|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.win32LobAppRegistryDetection"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.win32LobAppRegistryDetection",
  "check32BitOn64System": true,
  "keyPath": "String",
  "valueName": "String",
  "detectionType": "String",
  "operator": "String",
  "detectionValue": "String"
}
```



