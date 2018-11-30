---
title: plannerPlanContextDetailsCollection リソースの種類
description: " 値は、plannerPlanContextDetails オブジェクトです。"
ms.openlocfilehash: 843be37ae0abc73de19e72c655b18834b7f5c03e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27071908"
---
# <a name="plannerplancontextdetailscollection-resource-type"></a>plannerPlanContextDetailsCollection リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。


**PlannerPlanContextDetailsCollection**リソースでは、プランがリンクされている外部のコンテキストのコレクションを表します。 このリソースは、オープン型であり、 [plannerPlanDetails](plannerplandetails.md)オブジェクトの一部であります。 プロパティ名、プロパティ値のペアでは、アプリケーション固有のコンテキストの識別子値は、 [plannerPlanContextDetails](plannerplancontextdetails.md)オブジェクトです。


## <a name="properties"></a>プロパティ
クライアントでは、オープン型のプロパティを定義できます。 この場合、クライアントは、プロパティ名と外部のコンテキストを表す特徴的な識別子を使用する必要があります。 プロパティの値は、 [plannerPlanContextDetails](plannerplancontextdetails.md)オブジェクトである必要があります。 OData を基に、オープン型のプロパティ名は次の文字を含めることはできません: `.`、 `:`、 `@`、 `%`。 これらの文字は、URL エンコード形式にエンコードする必要があります。 お気に入りの一覧で項目を削除するに値が必要な[plannerPlanContextCollection](plannerplancontextcollection.md)コレクションから削除する代わりに、このオブジェクトのエントリを自動的に削除されます。


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerPlanContextDetailsCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->