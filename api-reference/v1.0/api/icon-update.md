---
title: アイコンを更新する
description: アイコン オブジェクトのプロパティを更新します。
ms.openlocfilehash: 0cb3b1af0369c86290c842232acc57792d1552ce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27023750"
---
# <a name="update-icon"></a>アイコンを更新する

アイコン オブジェクトのプロパティを更新します。
## <a name="permissions"></a>アクセス許可
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類      | アクセス許可 (特権の小さいものから大きいものへ)              | 
|:--------------------|:---------------------------------------------------------| 
|委任 (職場または学校のアカウント) | Files.ReadWrite    | 
|委任 (個人用 Microsoft アカウント) | サポートされていません。    | 
|アプリケーション | サポートされていません。 | 

## <a name="http-request"></a>HTTP 要求
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/sort/fields/icon
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/sort/fields/icon
```
## <a name="optional-request-headers"></a>オプションの要求ヘッダー
| 名前       | 説明|
|:-----------|:-----------|
| Authorization  | ベアラー {トークン}。必須。 |


## <a name="request-body"></a>要求本文
要求本文で、更新する関連フィールドの値を指定します。要求本文に含まれない既存のプロパティは、以前の値のままになるか、他のプロパティ値の変化に基づいて再計算されます。最適なパフォーマンスを得るためには、変更されていない既存の値を含めないでください。

| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|index|int|指定したセット内のアイコンのインデックスを表します。|
|set|文字列|一部であるアイコンのセットを表します。 可能な値: `Invalid`、 `ThreeArrows`、 `ThreeArrowsGray`、 `ThreeFlags`、 `ThreeTrafficLights1`、 `ThreeTrafficLights2`、 `ThreeSigns`、 `ThreeSymbols`、 `ThreeSymbols2`、 `FourArrows`、 `FourArrowsGray`、 `FourRedToBlack`、 `FourRating`、 `FourTrafficLights`、 `FiveArrows`、 `FiveArrowsGray`、 `FiveRating`、 `FiveQuarters`、 `ThreeStars`, `ThreeTriangles`, `FiveBoxes`.|

## <a name="response"></a>応答

成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で、更新された[アイコン](../resources/icon.md) オブジェクトを返します。
## <a name="example"></a>例
##### <a name="request"></a>要求
以下は、要求の例です。
<!-- {
  "blockType": "request",
  "name": "update_icon"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/sort/fields/icon
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```
##### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookIcon"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 39

{
  "set": "set-value",
  "index": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update icon",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->