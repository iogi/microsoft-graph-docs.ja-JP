---
title: ユーザーを更新する
description: ユーザー オブジェクトのプロパティを更新します。
ms.openlocfilehash: e1909d25e9cfd8281801ba0a398a3fc6901693bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067107"
---
# <a name="update-user"></a>ユーザーを更新する

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中で、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

[user](../resources/intune-shared-user.md) オブジェクトのプロパティを更新します。

## <a name="prerequisites"></a>前提条件

この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)||
| &nbsp; &nbsp; **デバイスの管理** | DeviceManagementManagedDevices.ReadWrite.All|
| &nbsp;&nbsp; **MAM** | DeviceManagementApps.ReadWrite.All|
| &nbsp;&nbsp; **契約時** | DeviceManagementServiceConfig.ReadWrite.All|
| &nbsp; &nbsp; **トラブルシューティング** | DeviceManagementManagedDevices.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a>要求ヘッダー

|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必須。|
|Accept|application/json|

## <a name="request-body"></a>要求本文

要求本文で、[user](../resources/intune-shared-user.md) オブジェクトの JSON 表記を指定します。

次の表に、[user](../resources/intune-shared-user.md) の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|ユーザーの一意識別子。|
|**契約時**|
|deviceEnrollmentLimit|Int32|ユーザーが登録を許可されているデバイスの最大数。 使用できる値は 5 または 1000 です。|

## <a name="response"></a>応答

成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [user](../resources/intune-shared-user.md) オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求

以下は、要求の例です。

``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a>応答

以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```


