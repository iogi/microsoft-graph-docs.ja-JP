---
title: WindowsOfficeClientSecurityConfiguration を更新します。
description: WindowsOfficeClientSecurityConfiguration オブジェクトのプロパティを更新します。
ms.openlocfilehash: 4e3430250a8b4332e07f9e6548c743aa122e1b19
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27069845"
---
# <a name="update-windowsofficeclientsecurityconfiguration"></a>WindowsOfficeClientSecurityConfiguration を更新します。

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

[WindowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトのプロパティを更新します。
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
PATCH /officeConfiguration/clientConfigurations/{officeClientConfigurationId}
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必須。|
|Accept|application/json|

## <a name="request-body"></a>要求本文
要求の本文に[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトの JSON の形式を指定します。

[WindowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)を作成するときに必要なプロパティを次の表に示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|Office クライアントの構成のポリシーの id。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|userPreferencePayload|Stream|JSON の環境設定は、バイナリ形式の文字列は、ユーザーがこれらの値をオーバーライドすることができます。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|policyPayload|Stream|JSON のポリシー設定はバイナリ形式の文字列は、ユーザーがこれらの値を変更することはできません。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|説明|String|管理者には、office クライアントの説明の構成のポリシーが用意されています。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|displayName|String|管理者は、office クライアントの構成のポリシーの名前を提供します。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|assignments|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)コレクション|一連のポリシーの割り当てをグループ化. [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|priority|Int32|優先度の値がテナントの下にある各ポリシーの一意の値にする必要があり、競合の解決に使用する、値が低い優先順位が高いことを意味します。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|lastModifiedDateTime|DateTime|ポリシーの最終変更された日付時刻スタンプ。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|userCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|ポリシーの概要チェックのユーザーです。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|
|checkinStatuses|[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)コレクション|Office クライアントでは、チェック状態の一覧です。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承されました。|



## <a name="response"></a>応答
かどうかは成功すると、このメソッドが返されます、`200 OK`応答コードおよび応答の本文に更新された[windowsOfficeClientSecurityConfiguration](../resources/intune-cirrus-windowsofficeclientsecurityconfiguration.md)オブジェクトです。

## <a name="example"></a>例
### <a name="request"></a>要求
以下は、要求の例です。
``` http
PATCH https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations/{officeClientConfigurationId}
Content-type: application/json
Content-length: 949

{
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "Description value",
  "displayName": "Display Name value",
  "priority": 8,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 2,
    "failedUserCount": 15
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "User Principal Name value",
      "deviceName": "Device Name value",
      "devicePlatform": "Device Platform value",
      "devicePlatformVersion": "Device Platform Version value",
      "wasSuccessful": true,
      "userId": "User Id value",
      "checkinDateTime": "2016-12-31T23:56:33.9571764-08:00",
      "errorMessage": "Error Message value",
      "appliedPolicies": [
        "Applied Policies value"
      ]
    }
  ]
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1077

{
  "@odata.type": "#microsoft.graph.windowsOfficeClientSecurityConfiguration",
  "id": "f90ca1a5-a1a5-f90c-a5a1-0cf9a5a10cf9",
  "userPreferencePayload": "<Unknown Primitive Type Edm.Stream>",
  "policyPayload": "<Unknown Primitive Type Edm.Stream>",
  "description": "Description value",
  "displayName": "Display Name value",
  "priority": 8,
  "userCheckinSummary": {
    "@odata.type": "microsoft.graph.officeUserCheckinSummary",
    "succeededUserCount": 2,
    "failedUserCount": 15
  },
  "checkinStatuses": [
    {
      "@odata.type": "microsoft.graph.officeClientCheckinStatus",
      "userPrincipalName": "User Principal Name value",
      "deviceName": "Device Name value",
      "devicePlatform": "Device Platform value",
      "devicePlatformVersion": "Device Platform Version value",
      "wasSuccessful": true,
      "userId": "User Id value",
      "checkinDateTime": "2016-12-31T23:56:33.9571764-08:00",
      "errorMessage": "Error Message value",
      "appliedPolicies": [
        "Applied Policies value"
      ]
    }
  ]
}
```


