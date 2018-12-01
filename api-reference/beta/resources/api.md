---
title: api リソースの種類
description: Web API アプリケーションの設定を指定します。
ms.openlocfilehash: b5b07ccb5a66027f9eb755754842f6e2e2ae708e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068798"
---
# <a name="api-resource-type"></a>api リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

Web API アプリケーションの設定を指定します。

## <a name="properties"></a>プロパティ

| プロパティ | 型 | 説明 |
|:---------------|:--------|:----------|
|requestedAccessTokenVersion|Int32| API の現在のリソースに許可されたアクセス トークンのバージョンを指定します。 使用可能な値は、1 または 2 です。  |
|oauth2PermissionScopes|[permissionScope](permissionscope.md)コレクション| Web アプリケーションの API (リソース) をクライアント アプリケーションに公開する OAuth 2.0 のアクセス許可のスコープのコレクション。 同意の中には、クライアント アプリケーションにこれらのアクセス許可のスコープを付与する可能性があります。 |

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.api"
}-->

```json
{
  "requestedAccessTokenVersion": 1,
  "oauth2PermissionScopes": [{"@odata.type": "microsoft.graph.permissionScope"}]
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "api resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->