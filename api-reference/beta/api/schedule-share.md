---
title: 'スケジュール: 共有'
description: スケジュールの時間範囲をスケジュールのメンバーと共有します。
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 3c1a35d8f9cb3ca31a8453983f1de0fa75ec79bb
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36364475"
---
# <a name="schedule-share"></a>スケジュール: 共有

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

スケジュールの[](../resources/schedule.md)時間範囲をスケジュールのメンバーと共有します。
指定されたチームメンバーによって表示可能な[スケジュール](../resources/schedule.md)の指定された時間範囲で、 [Shift](../resources/shift.md)と[timeoff](../resources/timeoff.md)の各アイテムのコレクションを作成します (従業員とマネージャーを含む)。
[スケジュール](../resources/schedule.md)内の各[シフト](../resources/shift.md)および[timeoff](../resources/timeoff.md)インスタンスでは、アイテムの下書きバージョンと共有バージョンがサポートされています。 下書きバージョンは、管理者のみが表示でき、共有バージョンは従業員とマネージャーに表示されます。 指定した時間範囲の各[シフト](../resources/shift.md)と[timeoff](../resources/timeoff.md)のインスタンスについては、共有アクションは下書きバージョンの共有バージョンを更新するので、マネージャーに加えて、アイテムに関する最新情報を表示することもできます。 **Notifyteam**パラメーターは、アイテムを表示できる従業員をさらに指定します。

## <a name="permissions"></a>アクセス許可

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント) | Group.ReadWrite.All    |
|委任 (個人用 Microsoft アカウント) | サポートされていません。    |
|アプリケーション | サポートされていません。 |

> **注**: この API は、管理者のアクセス許可をサポートします。 グローバル管理者は、所属していないグループにアクセスできます。

## <a name="http-request"></a>HTTP 要求

<!-- { "blockType": "ignored" } -->

```http
POST /teams/{teamId}/schedule/share
```

## <a name="request-headers"></a>要求ヘッダー

| ヘッダー       | 値 |
|:---------------|:--------|
| Authorization  | ベアラー {トークン}。必須。  |
| Content-Type  | application/json  |

## <a name="request-body"></a>要求本文

要求本文で、次のパラメーターを含む JSON オブジェクトを指定します。

|パラメーター                   |型           |説明  |
|-----------------------|-------------------|--------------|
| notifyTeam            |`Boolean`             |チーム全体がこのアクションの通知を表示するかどうかを指定します。または、共有されていた交代が割り当てられた従業員のみを取得します。 必須です。       |
| startDateTime         |`DateTimeOffset`   |スケジュールの開始時刻を開始する時刻。 必須です。   |
| endDateTime           |`DateTimeOffset`   | スケジュールによる移動を終了するまでの終了時刻。   |

## <a name="response"></a>応答

成功した場合、このメソッドは `204 No Content` 応答コードを返します。応答本文には何も返されません。

## <a name="example"></a>例

#### <a name="request"></a>要求

要求の例を次に示します。

# <a name="httptabhttp"></a>[プロトコル](#tab/http)
<!-- {
  "blockType": "request",
  "name": "schedule-share"
}-->
```http
POST https://graph.microsoft.com/beta/teams/{teamId}/schedule/share
Content-type: application/json

{
  "notifyTeam": true,
  "startDateTime": "2018-10-08T00:00:00.000Z",
  "endDateTime": "2018-10-15T00:00:00.000Z"
}
```
# <a name="ctabcsharp"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/schedule-share-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascripttabjavascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/schedule-share-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-ctabobjc"></a>[目的-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/schedule-share-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javatabjava"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/schedule-share-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


#### <a name="response"></a>応答

応答の例を次に示します。 

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.None"
} -->

```http
HTTP/1.1 204 No content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Shares a time-range of the schedule with the schedule members",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->
