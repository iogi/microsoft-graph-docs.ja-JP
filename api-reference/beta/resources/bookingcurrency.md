---
title: bookingCurrency リソースの種類
description: " > **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。"
ms.openlocfilehash: a68b88160e42217f3605c4a4bb30f692e8dafc06
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067927"
---
# <a name="bookingcurrency-resource-type"></a>bookingCurrency リソースの種類

 > **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。
 
[BookingBusiness](bookingbusiness.md)でサポートされている通貨の通貨を表します。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[リスト bookingCurrencies](../api/bookingcurrency-list.md) | [bookingCurrency](bookingcurrency.md)コレクション |Microsoft 予約業務に利用可能な**bookingCurrency**のオブジェクトの一覧を取得します。|
|[BookingCurrency を取得します。](../api/bookingcurrency-get.md) | [bookingCurrency](bookingcurrency.md) |**BookingCurrency**オブジェクトのプロパティを取得します。|


## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|id|String| [ISO 4217](https://www.iso.org/iso-4217-currency-codes.html)の 3 文字の通貨コード。 たとえば、米ドルの通貨コードは米ドル、オーストラリアの AUD. 読み取り専用。|
|シンボル|String| 通貨記号。 米ドルとオーストラリア ドルの通貨記号は $ です。  |

## <a name="relationships"></a>リレーションシップ
なし


## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.bookingCurrency"
}-->

```json
{
  "id": "String (identifier)",
  "symbol": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "bookingCurrency resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->