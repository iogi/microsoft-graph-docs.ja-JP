---
title: typedEmailAddress リソースの種類
description: 名前、電子メール アドレス、および連絡先の対応する電子メール アドレス タイプを表します。
ms.openlocfilehash: 3f40add32fbc219606b6d78041552fc108803d1c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27074407"
---
# <a name="typedemailaddress-resource-type"></a>typedEmailAddress リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

名前、電子メール アドレス、および、対応する電子メール アドレスの種類[にお問い合わせください](contact.md)を表します。

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|address|String|連絡先の電子メール アドレスです。|
|名前|String|連絡先の表示名。|
|type |String |電子メール アドレスの種類。 可能な値は、`unknown`、`work`、`personal`、`main`、`other` です。 既定値は、 `unknown`、つまり、**アドレス**が設定されていない特定の種類として。 |
|otherLabel |String  |電子メール アドレスのカスタムの型を指定する**の種類**を設定`other`、 **otherLabel**を独自の文字列を割り当てるとします。 など、ボランティア活動の特定の電子メール アドレスを使用する場合があります。 **タイプ**を設定`other`、 **otherLabel**を次のように独自の文字列を設定して`Volunteer work`。 |

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.typedEmailAddress"
}-->

```json
{
  "address": "string",
  "name": "string",
  "type": "string",
  "otherLabel": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "emailAddress resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->