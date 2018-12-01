---
title: privilegedRole リソースの種類
description: 次のように、Azure AD 管理者の役割を表します:**グローバル ・ アドミニストレーター、課金管理者、サービス管理者、ユーザー管理者、管理者のパスワード**などです。
ms.openlocfilehash: 0c04ab9de13732e4ac9eecb943a10945bec59d02
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067413"
---
# <a name="privilegedrole-resource-type"></a>privilegedRole リソースの種類

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

次のように、Azure AD 管理者の役割を表します:**グローバル ・ アドミニストレーター、課金管理者、サービス管理者、ユーザー管理者、管理者のパスワード**などです。


## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[PrivilegedRole オブジェクトのリスト](../api/privilegedrole-list.md) | [privilegedRole](privilegedrole.md)コレクション|PrivilegedRole のコレクションを取得します。|
|[PrivilegedRole を取得します。](../api/privilegedrole-get.md) | [privilegedRole](privilegedrole.md) |PrivilegedRole オブジェクトのプロパティと関係を参照してください。|
|[リストの割り当て](../api/privilegedrole-list-assignments.md) |[privilegedRoleAssignment](privilegedroleassignment.md)コレクション| このロールの割り当てオブジェクトのコレクションを取得します。|
|[selfActivate](../api/privilegedrole-selfactivate.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|割り当て済みのロールをアクティブにします。|
|[selfDeactivate](../api/privilegedrole-selfdeactivate.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|割り当て済みのロールを非アクティブ化します。|

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|ID|文字列|管理者の役割の一意の識別子です。 GUID の文字列し、特定の役割の Azure AD からロール テンプレートの id と同じ値を持ちます。 読み取り専用。|
|name|文字列|ロール名です。|

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|assignments|[privilegedRoleAssignment](privilegedroleassignment.md)コレクション| このロールの割り当て。 読み取り専用。 Null 許容型。|
|settings|[privilegedRoleSettings](privilegedrolesettings.md)| このロールの設定をします。 読み取り専用。 Null 許容型。|
|概要|[privilegedRoleSummary](privilegedrolesummary.md)| この役割の概要情報です。 読み取り専用。 Null 許容型。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRole"
}-->

```json
{
  "id": "string (identifier)",
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->