---
title: businessFlowTemplate リソースの種類
description: Azure AD にアクセス確認機能を`businesFlowTemplate`、Azure AD 業務フローのテンプレートを表します。 グループのゲスト メンバーを確認する場合など、テンプレートの識別子は、呼び出し元によって、アクセス確認を作成するときに提供されます。
ms.openlocfilehash: 8faf1a1381f5cdcf4bfaab78adc7a6554479b427
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27073212"
---
# <a name="businessflowtemplate-resource-type"></a>businessFlowTemplate リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

Azure AD[アクセスの確認](accessreviews-root.md)機能で、 `businesFlowTemplate` 、Azure AD 業務フローのテンプレートを表します。 グループのゲスト メンバーを確認する場合など、テンプレートの識別子は、呼び出し元によって、アクセス確認を作成するときに提供されます。

業務フローのテンプレート オブジェクトは、グローバル管理者 onboards アクセスを使用するテナント機能を確認するときに自動的に生成されます。  追加のビジネス フローのテンプレートは作成されません。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[リスト businessFlowTemplates](../api/businessflowtemplate-list.md) | [businessFlowTemplate](businessflowtemplate.md)コレクション| レビューにアクセスする適切なビジネス フローのテンプレートを取得します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
| `id`                     |`String`                | 業務フローのテンプレートの機能に割り当てられた識別子                                      |
| `displayName`            |`String`                | 業務フローのテンプレートの名前                                                             |


## <a name="relationships"></a>リレーションシップ

なし。

## <a name="see-also"></a>関連項目

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[AccessReview を作成します。](../api/accessreview-create.md) | [accessReview](accessreview.md) |   新しい accessReview を作成します。 |


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.businessFlowTemplate"
}-->

```json
{
 "id": "string (identifier)",
 "displayName": "string"
}

```

<!-- {
  "type": "#page.annotation",
  "description": "businessFlowTemplate resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->