# <a name="list-manageddevices"></a><span data-ttu-id="0a2f2-101">managedDevices のリスト</span><span class="sxs-lookup"><span data-stu-id="0a2f2-101">List managedDevices</span></span>

> <span data-ttu-id="0a2f2-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0a2f2-103">[managedDevice](../resources/intune_devices_manageddevice.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-103">List properties and relationships of the [managedDevice](../resources/intune_devices_manageddevice.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0a2f2-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="0a2f2-104">Prerequisites</span></span>
<span data-ttu-id="0a2f2-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0a2f2-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="0a2f2-107">Permission type</span></span>|<span data-ttu-id="0a2f2-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="0a2f2-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0a2f2-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="0a2f2-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0a2f2-110">DeviceManagementManagedDevices.ReadWrite.All、DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="0a2f2-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="0a2f2-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="0a2f2-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0a2f2-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-112">Not supported.</span></span>|
|<span data-ttu-id="0a2f2-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0a2f2-113">Application</span></span>|<span data-ttu-id="0a2f2-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0a2f2-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="0a2f2-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /users/{usersId}/managedDevices
GET /deviceManagement/managedDevices
GET /deviceManagement/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="0a2f2-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="0a2f2-116">Request headers</span></span>
|<span data-ttu-id="0a2f2-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="0a2f2-117">Header</span></span>|<span data-ttu-id="0a2f2-118">値</span><span class="sxs-lookup"><span data-stu-id="0a2f2-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0a2f2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0a2f2-119">Authorization</span></span>|<span data-ttu-id="0a2f2-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="0a2f2-121">Accept</span><span class="sxs-lookup"><span data-stu-id="0a2f2-121">Accept</span></span>|<span data-ttu-id="0a2f2-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0a2f2-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0a2f2-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="0a2f2-123">Request body</span></span>
<span data-ttu-id="0a2f2-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0a2f2-125">応答</span><span class="sxs-lookup"><span data-stu-id="0a2f2-125">Response</span></span>
<span data-ttu-id="0a2f2-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [managedDevice](../resources/intune_devices_manageddevice.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-126">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/intune_devices_manageddevice.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0a2f2-127">例</span><span class="sxs-lookup"><span data-stu-id="0a2f2-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="0a2f2-128">要求</span><span class="sxs-lookup"><span data-stu-id="0a2f2-128">Request</span></span>
<span data-ttu-id="0a2f2-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices
```

### <a name="response"></a><span data-ttu-id="0a2f2-130">応答</span><span class="sxs-lookup"><span data-stu-id="0a2f2-130">Response</span></span>
<span data-ttu-id="0a2f2-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 5086

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedDevice",
      "id": "705c034c-034c-705c-4c03-5c704c035c70",
      "userId": "User Id value",
      "deviceName": "Device Name value",
      "deviceActionResults": [
        {
          "@odata.type": "microsoft.graph.deviceActionResult",
          "actionName": "Action Name value",
          "actionState": "pending",
          "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
          "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
        }
      ],
      "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "operatingSystem": "Operating System value",
      "complianceState": "compliant",
      "jailBroken": "Jail Broken value",
      "managementAgent": "mdm",
      "osVersion": "Os Version value",
      "easActivated": true,
      "easDeviceId": "Eas Device Id value",
      "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
      "azureADRegistered": true,
      "deviceEnrollmentType": "userEnrollment",
      "activationLockBypassCode": "Activation Lock Bypass Code value",
      "emailAddress": "Email Address value",
      "azureADDeviceId": "Azure ADDevice Id value",
      "deviceRegistrationState": "registered",
      "deviceCategoryDisplayName": "Device Category Display Name value",
      "isSupervised": true,
      "exchangeLastSuccessfulSyncDateTime": "2017-01-01T00:00:45.8803083-08:00",
      "exchangeAccessState": "unknown",
      "exchangeAccessStateReason": "unknown",
      "remoteAssistanceSessionUrl": "https://example.com/remoteAssistanceSessionUrl/",
      "remoteAssistanceSessionErrorDetails": "Remote Assistance Session Error Details value",
      "isEncrypted": true,
      "userPrincipalName": "User Principal Name value",
      "model": "Model value",
      "manufacturer": "Manufacturer value",
      "imei": "Imei value",
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
      "serialNumber": "Serial Number value",
      "phoneNumber": "Phone Number value",
      "androidSecurityPatchLevel": "Android Security Patch Level value",
      "userDisplayName": "User Display Name value",
      "configurationManagerClientEnabledFeatures": {
        "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
        "inventory": true,
        "modernApps": true,
        "resourceAccess": true,
        "deviceConfiguration": true,
        "compliancePolicy": true,
        "windowsUpdateForBusiness": true
      },
      "wiFiMacAddress": "Wi Fi Mac Address value",
      "deviceHealthAttestationState": {
        "@odata.type": "microsoft.graph.deviceHealthAttestationState",
        "lastUpdateDateTime": "Last Update Date Time value",
        "contentNamespaceUrl": "https://example.com/contentNamespaceUrl/",
        "deviceHealthAttestationStatus": "Device Health Attestation Status value",
        "contentVersion": "Content Version value",
        "issuedDateTime": "2016-12-31T23:58:22.1231038-08:00",
        "attestationIdentityKey": "Attestation Identity Key value",
        "resetCount": 10,
        "restartCount": 12,
        "dataExcutionPolicy": "Data Excution Policy value",
        "bitLockerStatus": "Bit Locker Status value",
        "bootManagerVersion": "Boot Manager Version value",
        "codeIntegrityCheckVersion": "Code Integrity Check Version value",
        "secureBoot": "Secure Boot value",
        "bootDebugging": "Boot Debugging value",
        "operatingSystemKernelDebugging": "Operating System Kernel Debugging value",
        "codeIntegrity": "Code Integrity value",
        "testSigning": "Test Signing value",
        "safeMode": "Safe Mode value",
        "windowsPE": "Windows PE value",
        "earlyLaunchAntiMalwareDriverProtection": "Early Launch Anti Malware Driver Protection value",
        "virtualSecureMode": "Virtual Secure Mode value",
        "pcrHashAlgorithm": "Pcr Hash Algorithm value",
        "bootAppSecurityVersion": "Boot App Security Version value",
        "bootManagerSecurityVersion": "Boot Manager Security Version value",
        "tpmVersion": "Tpm Version value",
        "pcr0": "Pcr0 value",
        "secureBootConfigurationPolicyFingerPrint": "Secure Boot Configuration Policy Finger Print value",
        "codeIntegrityPolicy": "Code Integrity Policy value",
        "bootRevisionListInfo": "Boot Revision List Info value",
        "operatingSystemRevListInfo": "Operating System Rev List Info value",
        "healthStatusMismatchInfo": "Health Status Mismatch Info value",
        "healthAttestationSupportedStatus": "Health Attestation Supported Status value"
      },
      "subscriberCarrier": "Subscriber Carrier value",
      "meid": "Meid value",
      "totalStorageSpaceInBytes": 8,
      "freeStorageSpaceInBytes": 7,
      "managedDeviceName": "Managed Device Name value",
      "partnerReportedThreatState": "activated"
    }
  ]
}
```


