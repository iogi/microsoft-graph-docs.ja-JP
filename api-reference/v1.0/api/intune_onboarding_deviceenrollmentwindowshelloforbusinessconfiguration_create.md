# <a name="create-deviceenrollmentwindowshelloforbusinessconfiguration"></a>deviceEnrollmentWindowsHelloForBusinessConfiguration の作成

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

新しい [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) オブジェクトを作成します。
## <a name="prerequisites"></a>前提条件
この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。

|アクセス許可の種類|アクセス許可 (特権の大きいものから小さいものへ)|
|:---|:---|
|委任 (職場または学校のアカウント)|DeviceManagementServiceConfig.ReadWrite.All|
|委任 (個人用 Microsoft アカウント)|サポートされていません。|
|アプリケーション|サポートされていません。|

## <a name="http-request"></a>HTTP 要求
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceEnrollmentConfigurations
```

## <a name="request-headers"></a>要求ヘッダー
|ヘッダー|値|
|:---|:---|
|承認|ベアラー &lt;トークン&gt;が必須。|
|承諾|application/json|

## <a name="request-body"></a>要求本文
要求本文で、deviceEnrollmentWindowsHelloForBusinessConfiguration オブジェクトの JSON 表記を指定します。

次の表に、deviceEnrollmentWindowsHelloForBusinessConfiguration の作成時に必要なプロパティを示します。

|プロパティ|型|説明|
|:---|:---|:---|
|id|String|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|displayName|String|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|description|String|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|priority|Int32|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|createdDateTime|DateTimeOffset|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|lastModifiedDateTime|DateTimeOffset|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|version|Int32|まだ文書化されていません。[deviceEnrollmentConfiguration](../resources/intune_onboarding_deviceenrollmentconfiguration.md) から継承します|
|pinMinimumLength|Int32|まだ文書化されていません|
|pinMaximumLength|Int32|まだ文書化されていません|
|pinUppercaseCharactersUsage|String|まだ文書化されていません。可能な値は、`allowed`、`required`、`disallowed` です。|
|pinLowercaseCharactersUsage|String|まだ文書化されていません。可能な値は、`allowed`、`required`、`disallowed` です。|
|pinSpecialCharactersUsage|String|まだ文書化されていません。可能な値は、`allowed`、`required`、`disallowed` です。|
|state|String|まだ文書化されていません。可能な値は、`notConfigured`、`enabled`、`disabled` です。|
|securityDeviceRequired|Boolean|まだ文書化されていません|
|unlockWithBiometricsEnabled|Boolean|まだ文書化されていません|
|remotePassportEnabled|Boolean|まだ文書化されていません|
|pinPreviousBlockCount|Int32|まだ文書化されていません|
|pinExpirationInDays|Int32|まだ文書化されていません|
|enhancedBiometricsState|String|まだ文書化されていません。可能な値は、`notConfigured`、`enabled`、`disabled` です。|



## <a name="response"></a>応答
成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) オブジェクトを返します。

## <a name="example"></a>例
### <a name="request"></a>要求
以下は、要求の例です。
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations
Content-type: application/json
Content-length: 693

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "state": "enabled",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 5,
  "pinExpirationInDays": 3,
  "enhancedBiometricsState": "enabled"
}
```

### <a name="response"></a>応答
以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 801

{
  "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
  "id": "3068e0cd-e0cd-3068-cde0-6830cde06830",
  "displayName": "Display Name value",
  "description": "Description value",
  "priority": 8,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": 7,
  "pinMinimumLength": 0,
  "pinMaximumLength": 0,
  "pinUppercaseCharactersUsage": "required",
  "pinLowercaseCharactersUsage": "required",
  "pinSpecialCharactersUsage": "required",
  "state": "enabled",
  "securityDeviceRequired": true,
  "unlockWithBiometricsEnabled": true,
  "remotePassportEnabled": true,
  "pinPreviousBlockCount": 5,
  "pinExpirationInDays": 3,
  "enhancedBiometricsState": "enabled"
}
```



