---
title: 'privilegedRoleAssignment: makeEligible'
description: 対象となるように、役割の割り当てを確認します。 ロールの割り当ては、呼び出しの前に対象が既にいる場合は、何も行われません。 ロールの割り当ては、永続的なリクエスターは、ターゲットのユーザーと異なる場合は、ロールの割り当てができるようになり、ロールはターゲット ユーザーの非アクティブ化します。 リクエスターは、ターゲット ユーザーと役割は、セキュリティ管理者、またはロールの権限を持つ管理者を既定の有効期限を持つロールがアクティブになります。
ms.openlocfilehash: f39f508c7aeae4d85db92b43f406cd3497533e38
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067111"
---
# <a name="privilegedroleassignment-makeeligible"></a>privilegedRoleAssignment: makeEligible

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

対象となるように、役割の割り当てを確認します。 ロールの割り当ては、呼び出しの前に対象が既にいる場合は、何も行われません。 ロールの割り当ては、永続的なリクエスターは、ターゲットのユーザーと異なる場合は、ロールの割り当てができるようになり、ロールはターゲット ユーザーの非アクティブ化します。 リクエスターは、ターゲット ユーザーと役割は、セキュリティ管理者、またはロールの権限を持つ管理者を既定の有効期限を持つロールがアクティブになります。

## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

リクエスターでは、_ロールの権限を持つ管理者_のロールを持っている必要があります。 

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Directory.AccessAsUser.All    |
|委任 (個人用 Microsoft アカウント) | サポートされていません。    |
|アプリケーション | サポートされていません。 |

## <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
POST /privilegedRoleAssignments/{id}/makeEligible
```
## <a name="request-headers"></a>要求ヘッダー
| 名前       | 説明|
|:---------------|:----------|
| Authorization  | ベアラー {トークン}。必須。 |

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答

かどうかは成功すると、このメソッドを返します`200 OK`、応答の本体で応答コードと[privilegedRoleAssignment](../resources/privilegedroleassignment.md)のオブジェクトです。

テナントの PIM を登録する必要があることに注意してください。 それ以外の場合、HTTP 403 アクセス不可の状態コードが返されます。
## <a name="example"></a>例
以下は、この API を呼び出す方法の例です。
##### <a name="request"></a>要求
以下は、要求の例です。
<!-- {
  "blockType": "request",
  "name": "privilegedroleassignment_makeeligible"
}-->
```http
POST https://graph.microsoft.com/beta/privilegedRoleAssignments/{id}/makeEligible
```

##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 184

{
  "id": "id-value",
  "userId": "userId-value",
  "roleId": "roleId-value",
  "isElevated": true,
  "expirationDateTime": "2016-10-19T10:37:00Z",
  "resultMessage": "resultMessage-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleAssignment: makeEligible",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->