---
title: reportRoot の更新
description: reportRoot オブジェクトのプロパティを更新します。
author: rolyon
localization_priority: Normal
ms.prod: intune
doc_type: apiPageType
ms.openlocfilehash: 027340de400809e45e0051900b8afb460960be2f
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36347438"
---
# <a name="update-reportroot"></a>reportRoot の更新

> **重要:** Microsoft Graph の/ベータ版の Api は変更される可能性があります。 実稼働アプリケーションでは、これらの API の使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

[reportRoot](../resources/intune-shared-reportroot.md) オブジェクトのプロパティを更新します。
## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)||
| &nbsp; &nbsp; **デバイス構成** | DeviceManagementConfiguration.ReadWrite.All|
| &nbsp; &nbsp; **トラブルシューティング** | DeviceManagementManagedDevices.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /reports
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、[reportRoot](../resources/intune-shared-reportroot.md) オブジェクトの JSON 表記を指定します。

次の表に、[reportRoot](../resources/intune-shared-reportroot.md) の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|このエンティティの一意識別子。|



## <a name="response"></a>応答
成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [reportRoot](../resources/intune-shared-reportroot.md) オブジェクトを返します。

## <a name="example"></a>例
### <a name="request"></a>要求
以下は、要求の例です。
``` http
PATCH https://graph.microsoft.com/beta/reports
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 101

{
  "@odata.type": "#microsoft.graph.reportRoot",
  "id": "9ab6b3dd-b3dd-9ab6-ddb3-b69addb3b69a"
}
```






