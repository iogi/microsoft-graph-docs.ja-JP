---
title: OfficeClientConfigurationAssignment を作成する
description: 既存のポリシーにターゲットグループを追加します。
localization_priority: Normal
author: rolyon
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: b028449b33ce062db0899303b3d98b21af8fb8c3
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36322248"
---
# <a name="create-officeclientconfigurationassignment"></a>OfficeClientConfigurationAssignment を作成する

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

既存のポリシーにターゲットグループを追加します。

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
POST /officeConfiguration/clientConfigurations/{key}/assignments
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、officeClientConfigurationAssignment オブジェクトの JSON 表記を指定します。

次の表に、officeClientConfigurationAssignment の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|OfficeConfigurationAssignment の Id。|
|target|[officeConfigurationAssignmentTarget](../resources/intune-cirrus-officeconfigurationassignmenttarget.md)|管理者によって定義されたターゲットの割り当て。|



## <a name="response"></a>応答
成功した場合、このメソッド`200 Created`は応答コードと、応答本文で[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{key}/assignments
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
  "target": {
    "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
  }
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.officeClientConfigurationAssignment",
  "id": "804730f3-30f3-8047-f330-4780f3304780",
  "target": {
    "@odata.type": "microsoft.graph.officeConfigurationAssignmentTarget"
  }
}
```






