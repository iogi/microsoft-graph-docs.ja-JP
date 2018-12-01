---
title: onPremisesProvisioningError リソースの種類
description: Azure Active Directory への設置型のディレクトリを同期するときは、ユーザーとグループのエンティティのディレクトリ同期のエラーを表します。
ms.openlocfilehash: 7d5b15d99559ddf5b7692b7eac9664de7ec50f1e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27024193"
---
# <a name="onpremisesprovisioningerror-resource-type"></a>onPremisesProvisioningError リソースの種類

同期、オンプレミス Azure Active Directory へのディレクトリは、[ユーザー](user.md)と[グループ](group.md)のエンティティのディレクトリ同期のエラーを表します。

## <a name="properties"></a>プロパティ

| プロパティ | 型 | 説明 |
|:---------------|:--------|:----------|
|category|String| プロビジョニングのエラーのカテゴリです。 注意: 現時点が 1 つだけ使用可能な値です。 使用可能な値: *PropertyConflict* - は、プロパティの値が一意でないことを示します。 その他のオブジェクトには、プロパティに対して同じ値が含まれています。 |
|occurredDateTime|DateTimeOffset| 日付と時刻、エラーが発生しました。 |
|propertyCausingError|String| エラーの原因でディレクトリのプロパティの名前です。 現在使用可能な値: *UserPrincipalName*または*メタベース* |
|value|文字列| エラーの原因で、プロパティの値です。 |

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->