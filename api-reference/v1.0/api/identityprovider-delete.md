---
title: identityProvider を削除する
description: 既存の identityProvider を削除する
localization_priority: Priority
author: valnav
ms.prod: microsoft-identity-platform
ms.openlocfilehash: a09018011e87da383371ba41b1a046ddeb9002b5
ms.sourcegitcommit: d95f6d39a0479da6e531f3734c4029dc596b9a3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2019
ms.locfileid: "29649425"
---
# <a name="delete-identityprovider"></a>identityProvider を削除する

既存の [identityProvider](../resources/identityprovider.md) を削除します。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント)|IdentityProvider.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)| サポートされていません。|
|アプリケーション|サポートされていません。|

職場または学校のアカウントは、テナントのグローバル管理者のものである必要があります。

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->
```http
DELETE /identityProviders/{id}
```

## <a name="request-headers"></a>要求ヘッダー

|名前|説明|
|:---------------|:----------|
|Authorization|ベアラー {トークン}。必須。|

## <a name="request-body"></a>要求本文

このメソッドには、要求本文を指定しません。

## <a name="response"></a>応答

成功した場合、このメソッドは `204 No Content` 応答コードを返します。

## <a name="example"></a>例

次の例では、** identityProvider ** を削除します。

##### <a name="request"></a>要求

<!-- {
  "blockType": "request",
  "name": "delete-identityprovider"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/identityProviders/Amazon-OAuth
```

##### <a name="response"></a>応答

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete identityProvider",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->