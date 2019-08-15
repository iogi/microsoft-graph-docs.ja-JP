---
title: ディレクトリ設定を作成する
description: この API を使用して、directorySettingTemplates で利用可能なテンプレートに基づいて新しい設定を作成します。 これらの設定は、テナントレベルまたはオブジェクトレベルで行うことができます (現在はグループに対してのみ)。 作成要求では、テンプレートで定義されているすべての設定の settingValues を指定する必要があります。 グループ固有の設定では、グループのメンバーがゲストユーザーを招待できるかどうかを制御する設定のみが可能です。 これは、グループにゲストユーザーを追加する機能が一般に利用可能になったときに、この動作を制御します。
localization_priority: Normal
author: davidmu1
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: 5b44b8a8d21210f22f2431fb6d83fca94355bd60
ms.sourcegitcommit: 1066aa4045d48f9c9b764d3b2891cf4f806d17d5
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/15/2019
ms.locfileid: "36417167"
---
# <a name="create-a-directory-setting"></a>ディレクトリ設定を作成する

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

この API を使用して、directorySettingTemplates で利用可能なテンプレートに基づいて新しい設定を作成します。 これらの設定は、テナントレベルまたはオブジェクトレベルで行うことができます (現在はグループに対してのみ)。 作成要求では、テンプレートで定義されているすべての設定の settingValues を指定する必要があります。 グループ固有の設定では、グループのメンバーがゲストユーザーを招待できるかどうかを制御する設定のみが可能です。 これは、グループにゲストユーザーを追加する機能が一般に利用可能になったときに、この動作を制御します。

> **注**: この API のベータ版は、グループにのみ適用されます。 この API の/v1.0 バージョンが、 *groupSettings を作成*する名前に変更されました。

テンプレートと、ベータ版でサポートされているプロパティの一覧については、 [Directorysettingtemplate クエリ](https://developer.microsoft.com/graph/graph-explorer?request=directorySettingTemplates&version=beta)を使用してください。 (V2.0 エンドポイントの場合は、[ [Groupsettingtemplates](https://developer.microsoft.com/graph/graph-explorer?request=groupSettingTemplates&version=v1.0)] を呼び出します)。


## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Directory.ReadWrite.All、Directory.AccessAsUser.All    |
|委任 (個人用 Microsoft アカウント) | サポートされていません。    |
|アプリケーション | Directory.ReadWrite.All |

## <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
POST /settings
POST /groups/{id}/settings
```
## <a name="request-headers"></a>要求ヘッダー
| 名前       | 説明|
|:---------------|:----------|
| Authorization  | ベアラー {トークン}。必須。|

## <a name="request-body"></a>要求本文
要求本文で、 [Directorysetting](../resources/directorysetting.md)オブジェクトの JSON 表記を指定します。  ただし、設定の表示名は、参照される設定テンプレート名に基づいて設定されます。

## <a name="response"></a>応答

成功した場合、この`201 Created`メソッドは応答コードと、応答本文で[directorysetting](../resources/directorysetting.md)オブジェクトを返します。

## <a name="example"></a>例
##### <a name="request"></a>要求
以下は、要求の例です。

# <a name="httptabhttp"></a>[プロトコル](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_directorysetting_from_settings"
}-->
```http
POST https://graph.microsoft.com/beta/settings
Content-type: application/json
Content-length: 222

{
  "templateId": "templateId-value",
  "values": [
    {
      "name": "name-value",
      "value": "value-value"
    }
  ]
}
```
# <a name="ctabcsharp"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-directorysetting-from-settings-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-directorysetting-from-settings-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[目的-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-directorysetting-from-settings-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

要求本文で、 [Directorysetting](../resources/directorysetting.md)オブジェクトの JSON 表記を指定します。
##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directorySetting"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 244

{
    "@odata.context": "https://graph.microsoft.com/stagingbeta/$metadata#settings/$entity",
    "id": "id-value",
    "displayName": "displayName-value",
    "templateId": "templateId-value",
    "values": [
      {
        "name": "name-value",
        "value": "value-value"
      }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Create directorySetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
