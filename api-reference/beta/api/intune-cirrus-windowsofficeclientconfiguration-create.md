---
title: WindowsOfficeClientConfiguration を作成する
description: ターゲットグループを使用して、新しいセキュリティで保護されていないポリシーを作成します。
localization_priority: Normal
author: rolyon
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: dffd413ca369378f3e3eccdbd1d3452b4854a72d
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36328242"
---
# <a name="create-windowsofficeclientconfiguration"></a>WindowsOfficeClientConfiguration を作成する

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

ターゲットグループを使用して、新しいセキュリティで保護されていないポリシーを作成します。

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
POST /officeConfiguration/clientConfigurations
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)オブジェクトの JSON 表記を指定します。

次の表に、 [windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|Office クライアント構成ポリシーの Id。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|userPreferencePayload|Stream|プリファレンス設定 JSON 文字列はバイナリ形式です。これらの値はユーザーが上書きできます。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|policyPayload|Stream|ポリシー設定 JSON 文字列 (バイナリ形式) では、ユーザーがこれらの値を変更することはできません。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|description|String|管理者が提供する office クライアント構成ポリシーの説明。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|displayName|String|管理者が指定した office クライアント構成ポリシーの名前。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|assignments|[officeClientConfigurationAssignment](../resources/intune-cirrus-officeclientconfigurationassignment.md)コレクション|ポリシーのグループの割り当てのリスト。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|priority|Int32|優先度の値は、テナントの各ポリシーの一意の値である必要があり、競合の解決に使用されます。低い値は、優先度が高くなります。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|lastModifiedDateTime|DateTime|ポリシーの最終更新日時スタンプ。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|userCheckinSummary|[officeUserCheckinSummary](../resources/intune-cirrus-officeusercheckinsummary.md)|ポリシーのユーザーチェックインの概要。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|
|checkinStatuses|[officeClientCheckinStatus](../resources/intune-cirrus-officeclientcheckinstatus.md)コレクション|Office クライアントのチェックイン状態のリスト。 [OfficeClientConfiguration](../resources/intune-cirrus-officeclientconfiguration.md)から継承します。|



## <a name="response"></a>応答
成功した場合、このメソッド`201 Created`は応答コードと、応答本文で[windowsOfficeClientConfiguration](../resources/intune-cirrus-windowsofficeclientconfiguration.md)オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/beta/officeConfiguration/clientConfigurations
Content-type: application/json
Content-length: 1020

{
  "@odata.type": "#microsoft.graph.windowsOfficeClientConfiguration",
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
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1069

{
  "@odata.type": "#microsoft.graph.windowsOfficeClientConfiguration",
  "id": "13a5ac73-ac73-13a5-73ac-a51373aca513",
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






