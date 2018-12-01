---
title: 'ユーザー: translateExchangeIds'
description: 形式との間、Outlook に関連するリソースの識別子を変換します。
ms.openlocfilehash: 0c6e74ad0bb9676f261ed0202757b1e036b09c85
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27070918"
---
# <a name="user-translateexchangeids"></a>ユーザー: translateExchangeIds

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

形式との間、Outlook に関連するリソースの識別子を変換します。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

| アクセス許可の種類 | アクセス許可 (特権の小さいものから大きいものへ) |
|:----------------|:--------------------------------------------|
| 委任 (職場または学校のアカウント) | User.ReadBasic、User.Read、User.ReadWrite、User.ReadBasic.All、User.Read.All、User.ReadWrite.All |
| 委任 (個人用 Microsoft アカウント) | User.ReadBasic、User.Read、User.ReadWrite |
| アプリケーション | User.Read.All、User.ReadWrite.All |

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->

```http
POST /me/translateExchangeIds
POST /users/{id|userPrincipalName}/translateExchangeIds
```

## <a name="request-headers"></a>要求ヘッダー

| 名前 | 値 |
|:-----|:------|
| Authorization | ベアラー {トークン}。必須。 |

## <a name="request-body"></a>要求本文

| パラメーター | 型 | 説明 |
|:----------|:-----|:------------|
| inputIds | Edm.String コレクション | 変換識別子のコレクションです。 コレクション内のすべての識別子は、同じソース ID の種類を持つ必要があり、同じメールボックス内のアイテムにする必要があります。 このコレクションの最大サイズは、1000 の文字列です。 |
| sourceIdType | exchangeIdFormat | ID の種類の識別子の`InputIds`のパラメーターです。 |
| targetIdType | exchangeIdFormat | 要求された ID の種類に変換します。 |

### <a name="exchangeidformat-values"></a>exchangeIdFormat 値

| 値 | 説明 |
|:-------|:------------|
| エントリ Id | MAPI クライアントによって使用されるバイナリのエントリ ID の形式です。 |
| ewsId | Exchange Web サービス クライアントによって使用される ID 形式です。 |
| immutableEntryId | MAPI と互換性のある不変の ID 形式です。 |
| restId | Microsoft Graph で使用される既定の ID 形式です。 |
| restImmutableEntryId | Microsoft Graph で使用される ID の変更不可能な形式です。 |

## <a name="response"></a>応答

かどうかは成功すると、このメソッドを返します`200 OK`応答コードおよび応答の本文に[convertIdResult](../resources/meetingtimesuggestionsresult.md)のコレクションです。

## <a name="example"></a>使用例

次の使用例は、REST API の通常の形式から、複数の識別子を変換する方法を示しています (`restId`) に残りの部分の変更不可能な形式 (`restImmutableEntryId`)。

##### <a name="request"></a>要求

要求の例を次に示します。
<!-- {
  "blockType": "request",
  "name": "user_translateexchangeids"
}-->

```http
POST https://graph.microsoft.com/beta/me/translateExchangeIds
Content-Type: application/json

{
  "inputIds" : [
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
  ],
  "sourceIdType": "restId",
  "targetIdType": "restImmutableEntryId"
}
```

##### <a name="response"></a>応答

応答の例を次のとおりです。
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.convertIdResult",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/testexchangebeta/$metadata#Collection(microsoft.graph.convertIdResult)",
  "value": [
    {
      "sourceId": "{rest-formatted-id-1},
      "targetId": "{rest-immutable-formatted-id-1}"
    },
    {
      "sourceId": "{rest-formatted-id-2},
      "targetId": "{rest-immutable-formatted-id-2}"
    }
  ]
}
```