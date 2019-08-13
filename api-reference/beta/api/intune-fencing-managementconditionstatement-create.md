---
title: ManagementConditionStatement の作成
description: 新しい managementConditionStatement オブジェクトを作成します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 48f636aa83b73aa7d5c4eee38bb0d9e9c02656f0
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36355609"
---
# <a name="create-managementconditionstatement"></a>ManagementConditionStatement の作成

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

新しい[Managementconditionstatement](../resources/intune-fencing-managementconditionstatement.md)オブジェクトを作成します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementConfiguration.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|DeviceManagementConfiguration.ReadWrite.All|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/managementConditionStatements
POST /deviceManagement/managementConditions/{managementConditionId}/managementConditionStatements
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、managementConditionStatement オブジェクトの JSON 表記を指定します。

次の表に、managementConditionStatement の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|管理条件ステートメントの一意識別子。 作成時に割り当てられたシステム生成値。|
|displayName|String|管理条件ステートメントの管理者定義の名前。|
|description|String|管理条件ステートメントの管理者定義の説明。|
|createdDateTime|DateTimeOffset|管理条件ステートメントが作成された時刻。 サービス側を生成しました。|
|modifiedDateTime|DateTimeOffset|管理条件ステートメントが最後に変更された時刻。 サービス側を更新しました。|
|式|[managementConditionExpression](../resources/intune-fencing-managementconditionexpression.md)|管理条件ステートメントがアクティブ化/非アクティブ化されたかどうかを評価するために使用される管理条件ステートメント式。|
|eTag|String|管理条件ステートメントの ETag。 サービス側を更新しました。|
|アプリケーションのプラットフォーム|[devicePlatformType](../resources/intune-shared-deviceplatformtype.md)コレクション|この管理条件ステートメントの適用可能なプラットフォーム。
これは、管理条件ステートメントに関連付けられている管理条件を参照して、適用可能なプラットフォームの共通部分を検索することによって計算されます。 可能な値は、`android`、`androidForWork`、`iOS`、`macOS`、`windowsPhone81`、`windows81AndLater`、`windows10AndLater`、`androidWorkProfile`、`unknown` です。|



## <a name="response"></a>応答
成功した場合、このメソッド`201 Created`は応答コードと、応答本文で[managementconditionstatement](../resources/intune-fencing-managementconditionstatement.md)オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/beta/deviceManagement/managementConditionStatements
Content-type: application/json
Content-length: 323

{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
  "displayName": "Display Name value",
  "description": "Description value",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ]
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 491

{
  "@odata.type": "#microsoft.graph.managementConditionStatement",
  "id": "bedb0c00-0c00-bedb-000c-dbbe000cdbbe",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "modifiedDateTime": "2017-01-01T00:00:22.8983556-08:00",
  "expression": {
    "@odata.type": "microsoft.graph.managementConditionExpression"
  },
  "eTag": "ETag value",
  "applicablePlatforms": [
    "androidForWork"
  ]
}
```






