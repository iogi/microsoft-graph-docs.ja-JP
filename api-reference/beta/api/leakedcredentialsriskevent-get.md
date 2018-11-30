---
title: LeakedCredentialsRiskEvent を取得します。
description: プロパティと、leakedcredentialsriskevent オブジェクトの関係を取得します。
ms.openlocfilehash: a3d259f785d2c8d6717f4dfe90ba04aeb454a1bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27073855"
---
# <a name="get-leakedcredentialsriskevent"></a>LeakedCredentialsRiskEvent を取得します。

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

プロパティと、leakedcredentialsriskevent オブジェクトの関係を取得します。
## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | IdentityRiskEvent.Read.All    |
|委任 (個人用 Microsoft アカウント) | サポートされていません。    |
|アプリケーション | IdentityRiskEvent.Read.All |

## <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
GET /leakedCredentialsRiskEvents/{id}
```
## <a name="request-headers"></a>要求ヘッダー
| 名前      |説明|
|:----------|:----------|
| Authorization  | ベアラー {トークン}。必須。 |
| Workbook-Session-Id  | 変更を保持するかどうかを決定するブック セッション ID。省略可能。|

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答

かどうかは成功すると、このメソッドが返されます、 `200 OK` 、応答の本体で応答コードと[leakedCredentialsRiskEvent](../resources/leakedcredentialsriskevent.md)のオブジェクトです。
## <a name="example"></a>例
##### <a name="request"></a>要求
以下は、要求の例です。
<!-- {
  "blockType": "request",
  "name": "get_leakedcredentialsriskevent"
}-->
```http
GET https://graph.microsoft.com/v1.0/leakedCredentialsRiskEvents/8c793a18-c86a-b5f9-7d9a-b3d024f33eee-278dc452-4163-dbc6-84eb-a050c37fc931-1a01abd3-b87a-cece-3f4d-c788b055c182
```
##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.leakedCredentialsRiskEvent"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 251

{
  "closedDateTime": null,
  "createdDateTime": "2016-01-29T00:01:49.126468Z",
  "id": "8c793a18-c86a-b5f9-7d9a-b3d024f33eee-278dc452-4163-dbc6-84eb-a050c37fc931-1a01abd3-b87a-cece-3f4d-c788b055c182",
  "riskEventDateTime": "2016-01-29T00:00:56.2255665Z",
  "riskEventStatus": "active",
  "riskLevel": "high",
  "riskType": "LeakedCredentialsRiskEvent",
  "userDisplayName": "Jon Doe",
  "userId": "278dc452-4163-dbc6-84eb-a050c37fc931",
  "userPrincipalName": "jon@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get leakedCredentialsRiskEvent",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->