---
title: AccessReview を取得します。
description: 'Azure AD のレビュー機能にアクセス、accessReview オブジェクトを取得します。  '
ms.openlocfilehash: ecd802613e6ab36816800197c00595c90426fb2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068002"
---
# <a name="get-accessreview"></a>AccessReview を取得します。

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

Azure AD[アクセスの確認](../resources/accessreviews-root.md)機能では、 [accessReview](../resources/accessreview.md)オブジェクトを取得します。  

アクセス レビューのレビュー担当者を取得するには、 [accessReview の校閲者の一覧](accessreview-listreviewers.md)API を使用します。 アクセス レビューの決定を取得するには、 [] ボックスの一覧 accessReview の意思決定](accessreview-listdecisions.md)の API、または[私の accessReview の決定事項を表示](accessreview-listmydecisions.md)API を使用します。

定期的なアクセス確認の場合を使用して、 `instances` 、過去、現在および将来のインスタンスのアクセス確認の[accessReview](../resources/accessreview.md)のコレクションを取得するために関係します。

## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類                        | アクセス許可 (特権の小さいものから大きいものへ)              |
|:--------------------------------------|:---------------------------------------------------------|
|委任 (職場または学校のアカウント)     | `AccessReview.Read.All`, `AccessReview.ReadWrite.All`.  サインインしているユーザーは、ディレクトリの役割をアクセスのレビューを読むことを許可またはアクセスのレビューのレビュー担当者として割り当てられている必要があります。 |
|委任 (個人用 Microsoft アカウント) | サポートされていません。 |
|アプリケーション                            | サポートされていません。 |

## <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
GET /accessReviews('{reviewId}')
```
## <a name="request-headers"></a>要求ヘッダー
| 名前         | 型        | 説明 |
|:-------------|:------------|:------------|
| Authorization | string | ベアラー\{トークン\}。 必須。 |

## <a name="request-body"></a>要求本文
要求の本体を提供する必要がありません。

## <a name="response"></a>応答
かどうかは成功すると、このメソッドが返されます、`200, OK`応答コードおよび応答の本文内の[accessReview](../resources/accessreview.md)オブジェクトです。

## <a name="example"></a>例
##### <a name="request"></a>要求

<!-- {
  "blockType": "request",
  "name": "get_accessReview"
}-->
```http
GET https://graph.microsoft.com/beta/accessReviews('2b83cc42-09db-46f6-8c6e-16fec466a82d')
```

##### <a name="response"></a>応答
>**注:** 読みやすくするために、ここに示す応答オブジェクトは短くされている場合があります。実際の呼び出しからは、すべてのプロパティが返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReview",
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
    "displayName": "review",
    "startDateTime": "2017-11-14T01:14:54.89Z",
    "endDateTime": "2017-12-14T01:14:54.89Z",
    "status": "InProgress",
    "businessFlowTemplateId": "6e4f3d20-c5c3-407f-9695-8460952bcc68",
    "reviewerType": "self",
    "description": "",
    "settings": {
        "reviewId": "2b83cc42-09db-46f6-8c6e-16fec466a82d",
        "mailNotificationsEnabled": true,
        "remindersEnabled": true,
        "justificationRequiredOnApproval": true,
        "recurrenceSettings": {
            "recurrenceType": "onetime",
            "recurrenceEndType": "endBy",
            "durationInDays": 0,
            "recurrenceCount": 0
        }
    }
}
```

## <a name="see-also"></a>関連項目

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[AccessReview を作成します。](accessreview-create.md) |    [accessReview](../resources/accessreview.md) |  新しい accessReview を作成します。 |
|[リスト programControls](programcontrol-list.md) | [デバッギング](../resources/programcontrol.md)コレクション | テナント内の programControls を一覧表示します。 |
|[AccessReview の校閲者の一覧](accessreview-listreviewers.md) |     コレクションを[割り当てられていません](../resources/useridentity.md)|    AccessReview のレビュー担当者を取得します。 |
|[リストの accessReview の決定](accessreview-listdecisions.md) |     [accessReviewDecision](../resources/accessreviewdecision.md)コレクション|    AccessReview の決定を取得します。|
|[マイ accessReview の決定事項を表示します。](accessreview-listmydecisions.md) |        [accessReviewDecision](../resources/accessreviewdecision.md)コレクション|    参照者、accessReview の自分の意思決定を取得します。|


<!-- {
  "type": "#page.annotation",
  "description": "Get accessReview",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->