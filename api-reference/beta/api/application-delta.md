---
title: 'アプリケーション: デルタ'
description: Get を新しく作成するには、更新、または全体のリソースのコレクションのすべての読み取りを実行しなくてもアプリケーションを削除します。 詳細については、デルタのクエリを使用するを参照してください。
ms.openlocfilehash: 6393e9a1340b2867e37a1f9f350ff50f2ba8a1cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068032"
---
# <a name="application-delta"></a>アプリケーション: デルタ

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

Get を新しく作成するには、更新、または全体のリソースのコレクションのすべての読み取りを実行しなくてもアプリケーションを削除します。 詳細については、[デルタのクエリを使用する](/graph/delta-query-overview)を参照してください。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。


|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Directory.Read.All、Directory.ReadWrite.All、Directory.AccessAsUser.All    |
|委任 (個人用 Microsoft アカウント) | サポートされていません。    |
|アプリケーション | Application.ReadWrite.All、Directory.Read.All |

## <a name="http-request"></a>HTTP 要求

変更の追跡を開始するには、アプリケーション リソースにデルタ関数を含む要求を行います。 

<!-- { "blockType": "ignored" } -->
```http
GET /applications/delta
```

### <a name="query-parameters"></a>クエリ パラメーター

変更を追跡する一連の 1 つまたは複数の**delta**関数の呼び出しが発生します。 任意のクエリ パラメーターを使用する場合 (以外の`$deltatoken`と`$skiptoken`)、**デルタ**の初期要求で指定する必要があります。 Microsoft Graph が自動的に任意指定のパラメーターをエンコードのトークンの部分に、`nextLink`または`deltaLink`の応答で提供される URL です。 必要なクエリ パラメーターを前もって 1 回指定しておくだけで済みます。 その後の要求では、前の応答で得られた `nextLink` や `deltaLink` の URL をコピーして適用します。エンコード済みの必要なパラメーターがこの URL に既に含まれているためです。

| クエリ パラメーター      | 種類   |説明|
|:---------------|:--------|:----------|
| $deltatoken | 文字列 | 返される[トークンの状態](/graph/delta-query-overview)、`deltaLink`の変更の追跡には、そのラウンドの完了を示す前の**デルタ**関数呼び出し、同じリソースを収集するための URL です。 保存し、全体を適用する`deltaLink`コレクションの変更履歴の次のラウンドの最初の要求にこのトークンを含む URL です。|
| $skiptoken | 文字列 | 返される[トークンの状態](/graph/delta-query-overview)、`nextLink`で同じリソースのコレクションを追跡するにさらに変更が加えられたことを示す前の**デルタ**関数の呼び出しの URL です。 |

## <a name="optional-query-parameters"></a>オプションのクエリ パラメーター

このメソッドは、応答をカスタマイズするための OData クエリ パラメーターをサポートします。

- 任意の GET リクエストと同様に `$select` クエリ パラメーターを使用して、最善のパフォーマンスを得るために必要なプロパティのみを指定することができます。_Id_ プロパティは常に返されます。 

- サポートが制限されて`$filter`。
  * サポートされる唯一の`$filter`の id で特定のリソースに対する変更を追跡するための式が:`$filter=id+eq+{value}`または`$filter=id+eq+{value1}+or+id+eq+{value2}`。 URL の最大長を指定することができます id の数が制限されます。


## <a name="request-headers"></a>要求ヘッダー
| 名前       | 説明|
|:---------------|:----------|
| Authorization  | Bearer &lt;token&gt;|
| Content-Type  | application/json |

## <a name="request-body"></a>要求本文
このメソッドには、要求本文を指定しません。

### <a name="response"></a>応答

かどうかは成功すると、このメソッドを返します`200 OK`、応答の本体で応答コードと[アプリケーション](../resources/application.md)コレクションのオブジェクトです。 応答には、nextLink URL または deltaLink の URL も含まれています。 

- 場合、`nextLink`の URL が返されますが、セッション内で取得するデータのページを追加します。 アプリケーションの継続を使用して要求を作成する、`nextLink`までの URL を`deltaLink`URL が応答に含まれています。

- 場合、`deltaLink`の URL が返される、返されるリソースの既存の状態に関する多くのデータはありません。 永続化し、使用して、 `deltaLink` 、将来的にリソースへの変更に関する説明への URL です。

参照先:</br>
- 詳細については、「[デルタ クエリの使用](/graph/delta-query-overview)」をご覧ください</br>
- 要求の例については、「[ユーザーに対する増分の変更の取得](/graph/delta-query-users)」をご覧ください。</br>

### <a name="example"></a>例
##### <a name="request"></a>要求
<!-- {
  "blockType": "request",
  "name": "application_delta"
}-->
```http
GET https://graph.microsoft.com/beta/applications/delta
```

##### <a name="response"></a>応答
注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- { 
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.application",
  "isCollection": true 
} --> 
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/beta/$metadata#applications",
  "@odata.nextLink":"https://graph.microsoft.com/beta/applications/delta?$skiptoken=pqwSUjGYvb3jQpbwVAwEL7yuI3dU1LecfkkfLPtnIjsXoYQp_dpA3cNJWc",
  "value": [
    {
      "api": {
        "acceptedAccessTokenVersion": 1,
        "publishedPermissionScopes": [
          {
            "adminConsentDescription": "adminConsentDescription-value",
            "adminConsentDisplayName": "adminConsentDisplayName-value",
            "id": "id-value",
            "isEnabled": true,
            "type": "type-value",
            "userConsentDescription": "userConsentDescription-value",
            "userConsentDisplayName": "userConsentDisplayName-value",
            "value": "value-value"
          }
        ]
      },
      "allowPublicClient": true,
      "applicationAliases": [
        "applicationAliases-value"
      ],
      "createdDateTime": "datetime-value",
      "installedClients": {
        "redirectUrls": [
          "redirectUrls-value"
        ]
      }
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "application: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->