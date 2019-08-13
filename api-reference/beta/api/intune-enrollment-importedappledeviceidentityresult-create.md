---
title: ImportedAppleDeviceIdentityResult を作成する
description: 新しい importedAppleDeviceIdentityResult オブジェクトを作成します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: apiPageType
ms.openlocfilehash: 02a673d4128c917c8368ec895cc493998e7066f2
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36356509"
---
# <a name="create-importedappledeviceidentityresult"></a>ImportedAppleDeviceIdentityResult を作成する

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

新しい[importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)オブジェクトを作成します。

## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementServiceConfig.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|DeviceManagementServiceConfig.ReadWrite.All|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|Authorization|ベアラー &lt;トークン&gt; が必要です。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、importedAppleDeviceIdentityResult オブジェクトの JSON 表記を指定します。

次の表に、importedAppleDeviceIdentityResult の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|エンティティのキー。 [ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承します。|
|シリアル番号|String|[ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されたデバイスのシリアル番号|
|requestedEnrollmentProfileId|String|登録プロファイル Id 管理者は、 [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承した次の登録時にデバイスに適用する予定です。|
|requestedEnrollmentProfileAssignmentDateTime|DateTimeOffset|時間登録プロファイルが[importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されたデバイスに割り当てられています。|
|isSupervised|Boolean|Apple デバイスが監視されているかどうかを示します。 詳細についてはhttps://support.apple.com/en-us/HT202837 、「 [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承する」を参照してください。|
|discoverySource|[discoverySource](../resources/intune-enrollment-discoverysource.md)|Apple デバイスの検出ソース。 [ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されます。 可能な値は、`unknown`、`adminImport`、`deviceEnrollmentProgram` です。|
|createdDateTime|DateTimeOffset|[ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されたデバイスの日時の作成日時|
|lastContactedDateTime|DateTimeOffset|[ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されたデバイスの最後の連絡日時。|
|description|String|[ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されたデバイスの説明|
|enrollmentState|[enrollmentState](../resources/intune-enrollment-enrollmentstate.md)|[ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承された Intune のデバイスの状態。 使用可能な値: `unknown`、`enrolled`、`pendingReset`、`failed`、`notContacted`、`blocked`。|
|platform|[プラットフォーム](../resources/intune-enrollment-platform.md)|デバイスのプラットフォーム。 [ImportedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)から継承されます。 使用可能な値: `unknown`、`ios`、`android`、`windows`、`windowsMobile`、`macOS`。|
|status|Boolean|インポートされたデバイス id の状態|



## <a name="response"></a>応答
成功した場合、このメソッド`201 Created`は応答コードと、応答本文で[importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md)オブジェクトを返します。

## <a name="example"></a>例

### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities
Content-type: application/json
Content-length: 522

{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 630

{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
  "id": "557cfb4a-fb4a-557c-4afb-7c554afb7c55",
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```






