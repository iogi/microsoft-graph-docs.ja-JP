---
title: iosCustomConfiguration の作成
description: 新しい iosCustomConfiguration オブジェクトを作成します。
ms.openlocfilehash: a301d959e21ad65d85c6b1fe27cd6b8366097edb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27021105"
---
# <a name="create-ioscustomconfiguration"></a>iosCustomConfiguration の作成

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

新しい [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) オブジェクトを作成します。
## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementConfiguration.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必須。|
|Accept|application/json|

## <a name="request-body"></a>要求本文
要求本文で、iosCustomConfiguration オブジェクトの JSON 表記を指定します。

次の表に、iosCustomConfiguration の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|オブジェクトが最後に変更された DateTime。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|createdDateTime|DateTimeOffset|オブジェクトが作成された DateTime。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|説明|String|デバイス構成について管理者が提供した説明。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|displayName|String|デバイス構成について管理者が指定した名前。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|version|Int32|デバイス構成のバージョン。 [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) から継承します|
|payloadName|String|ユーザーに表示される名前。|
|payloadFileName|String|ペイロード ファイル名 (*.mobileconfig | *.xml)。|
|payload|Binary|ペイロード。 (UTF8 でエンコードされたバイト配列)|



## <a name="response"></a>応答
成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [iosCustomConfiguration](../resources/intune-deviceconfig-ioscustomconfiguration.md) オブジェクトを返します。

## <a name="example"></a>例
### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 279

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 451

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "id": "f34428e3-28e3-f344-e328-44f3e32844f3",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```


