---
title: educationResource リソースの種類
description: システム内のすべてのリソース オブジェクトのスーパークラスです。 リソースは**割り当て**または**送信**される学習オブジェクトを表す、あるいはその両方に関連付けられています。
ms.openlocfilehash: b7e64a946992bb0b43c5bfe50e8d92b5f7176856
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27071885"
---
# <a name="educationresource-resource-type"></a>educationResource リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

システム内のすべてのリソース オブジェクトのスーパークラスです。 リソースは**割り当て**または**送信**される学習オブジェクトを表す、あるいはその両方に関連付けられている割り当てられるまたは渡されました。 リソースを直接インスタンス化できません。使用されているリソースの種類を表すサブクラス化を行う必要があります。

このリソースは、すべての種類のリソース間で共通のプロパティを格納します。


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|リソースを作成したとします。|
|createdDateTime|リソースが作成された時点。  DateTimeOffset|Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、必ず UTC 時間です。たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|
|displayName|String|リソースの名前を表示します。|
|lastModifiedBy|[identitySet](identityset.md)|ユーザーがリソースを変更する最後のユーザーです。|
|lastModifiedDateTime|DateTimeOffset|リソースが最後に修正された瞬間です。  Timestamp 型は、ISO 8601 形式を使用して日付と時刻の情報を表し、常に UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'`|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationResource"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->