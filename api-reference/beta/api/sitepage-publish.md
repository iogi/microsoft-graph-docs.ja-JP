---
author: rahmit
ms.author: rahmit
ms.date: 09/10/2018
title: '[発行] ページ'
ms.openlocfilehash: d932b1d37b5ab81f86f6e87aab43aa1cf9dc3eae
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068068"
---
# <a name="sitepage-publish"></a>sitePage: 発行

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

ページのバージョンをすべてのユーザーが使用可能にする[sitePage][]リソースの最新バージョンを公開します。 ページがチェック アウトされている場合は、ページをチェックインし、公開します。 この API の呼び出し元ページがチェック アウトされた場合ページが自動的にチェックインし、公開します。

[sitePage]: ../resources/sitepage.md

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Files.ReadWrite、Files.ReadWrite.All、Sites.ReadWrite.All    |
|委任 (個人用 Microsoft アカウント) | Files.ReadWrite、Files.ReadWrite.All    |
|アプリケーション | Files.ReadWrite.All、Sites.ReadWrite.All |

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{siteId}/pages/{pageId}/publish
```

## <a name="request-body"></a>要求本文

このメッセージには、要求の本体がありません。 送信の要求の本文は無視されます。

## <a name="response"></a>応答

成功すると、API 呼び出しは `204 No Content` を返します。

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```


<!-- {
  "type": "#page.annotation",
  "description": "Publish a page.",
  "keywords": "publish page",
  "section": "documentation",
  "tocPath": "Pages/Publish"
} -->