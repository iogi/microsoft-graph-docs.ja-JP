---
title: auditEvent リソース タイプ
description: 監査イベントのプロパティが含まれるクラス。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 5893d14fdd1f1e274a355526d51bda5519a16b93
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36335257"
---
# <a name="auditevent-resource-type"></a>auditEvent リソース タイプ

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

監査イベントのプロパティが含まれるクラス。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[List auditEvents](../api/intune-auditing-auditevent-list.md)|[auditEvent](../resources/intune-auditing-auditevent.md) コレクション|[auditEvent](../resources/intune-auditing-auditevent.md) オブジェクトのプロパティとリレーションシップをリストします。|
|[Get auditEvent](../api/intune-auditing-auditevent-get.md)|[auditEvent](../resources/intune-auditing-auditevent.md)|[auditEvent](../resources/intune-auditing-auditevent.md) オブジェクトのプロパティとリレーションシップを読み取ります。|
|[Create auditEvent](../api/intune-auditing-auditevent-create.md)|[auditEvent](../resources/intune-auditing-auditevent.md)|新しい [auditEvent](../resources/intune-auditing-auditevent.md) オブジェクトを作成します。|
|[Delete auditEvent](../api/intune-auditing-auditevent-delete.md)|なし|[auditEvent](../resources/intune-auditing-auditevent.md) を削除します。|
|[Update auditEvent](../api/intune-auditing-auditevent-update.md)|[auditEvent](../resources/intune-auditing-auditevent.md)|[auditEvent](../resources/intune-auditing-auditevent.md) オブジェクトのプロパティを更新します。|
|[getAuditCategories function](../api/intune-auditing-auditevent-getauditcategories.md)|String コレクション|まだ文書化されていません|
|[getAuditActivityTypes function](../api/intune-auditing-auditevent-getauditactivitytypes.md)|String コレクション|まだ文書化されていません|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。|
|displayName|String|イベントの表示名。|
|componentName|String|コンポーネント名。|
|actor|[auditActor](../resources/intune-auditing-auditactor.md)|監査イベントに関連付けられている AAD ユーザーとアプリケーション。|
|activity|String|わかりやすいアクティビティの名前。|
|activityDateTime|DateTimeOffset|アクティビティが実行された日時 (UTC)。|
|activityType|String|実行されたアクティビティの種類。|
|activityOperationType|String|アクティビティの HTTP 操作の種類。|
|activityResult|String|アクティビティの結果。|
|correlationId|Guid|システム内でのアクティビティに関連付けるために使用されるクライアント要求 ID。|
|resources|[auditResource](../resources/intune-auditing-auditresource.md) コレクション|変更中のリソースです。|
|category|String|監査のカテゴリです。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.auditEvent"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.auditEvent",
  "id": "String (identifier)",
  "displayName": "String",
  "componentName": "String",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "String",
    "userPermissions": [
      "String"
    ],
    "applicationId": "String",
    "applicationDisplayName": "String",
    "userPrincipalName": "String",
    "servicePrincipalName": "String",
    "ipAddress": "String",
    "userId": "String"
  },
  "activity": "String",
  "activityDateTime": "String (timestamp)",
  "activityType": "String",
  "activityOperationType": "String",
  "activityResult": "String",
  "correlationId": "Guid",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "String",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "String",
          "oldValue": "String",
          "newValue": "String"
        }
      ],
      "type": "String",
      "resourceId": "String"
    }
  ],
  "category": "String"
}
```



