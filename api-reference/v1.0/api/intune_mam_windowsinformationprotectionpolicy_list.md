# <a name="list-windowsinformationprotectionpolicies"></a><span data-ttu-id="edbbc-101">windowsInformationProtectionPolicies のリスト</span><span class="sxs-lookup"><span data-stu-id="edbbc-101">List windowsInformationProtectionPolicies</span></span>

> <span data-ttu-id="edbbc-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edbbc-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="edbbc-103">[windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="edbbc-103">List properties and relationships of the [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="edbbc-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="edbbc-104">Prerequisites</span></span>
<span data-ttu-id="edbbc-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="edbbc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="edbbc-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="edbbc-107">Permission type</span></span>|<span data-ttu-id="edbbc-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="edbbc-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="edbbc-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="edbbc-109">Delegated (work or school account)</span></span>|<span data-ttu-id="edbbc-110">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="edbbc-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="edbbc-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="edbbc-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="edbbc-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edbbc-112">Not supported.</span></span>|
|<span data-ttu-id="edbbc-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="edbbc-113">Application</span></span>|<span data-ttu-id="edbbc-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edbbc-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="edbbc-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="edbbc-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/windowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="edbbc-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="edbbc-116">Request headers</span></span>
|<span data-ttu-id="edbbc-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="edbbc-117">Header</span></span>|<span data-ttu-id="edbbc-118">値</span><span class="sxs-lookup"><span data-stu-id="edbbc-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="edbbc-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="edbbc-119">Authorization</span></span>|<span data-ttu-id="edbbc-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="edbbc-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="edbbc-121">Accept</span><span class="sxs-lookup"><span data-stu-id="edbbc-121">Accept</span></span>|<span data-ttu-id="edbbc-122">application/json</span><span class="sxs-lookup"><span data-stu-id="edbbc-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="edbbc-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="edbbc-123">Request body</span></span>
<span data-ttu-id="edbbc-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="edbbc-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="edbbc-125">応答</span><span class="sxs-lookup"><span data-stu-id="edbbc-125">Response</span></span>
<span data-ttu-id="edbbc-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="edbbc-126">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/intune_mam_windowsinformationprotectionpolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="edbbc-127">例</span><span class="sxs-lookup"><span data-stu-id="edbbc-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="edbbc-128">要求</span><span class="sxs-lookup"><span data-stu-id="edbbc-128">Request</span></span>
<span data-ttu-id="edbbc-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="edbbc-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies
```

### <a name="response"></a><span data-ttu-id="edbbc-130">応答</span><span class="sxs-lookup"><span data-stu-id="edbbc-130">Response</span></span>
<span data-ttu-id="edbbc-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="edbbc-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 5155

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
      "displayName": "Display Name value",
      "description": "Description value",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "id": "6397be61-be61-6397-61be-976361be9763",
      "version": "Version value",
      "enforcementLevel": "encryptAndAuditOnly",
      "enterpriseDomain": "Enterprise Domain value",
      "enterpriseProtectedDomainNames": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "protectionUnderLockConfigRequired": true,
      "dataRecoveryCertificate": {
        "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
        "subjectName": "Subject Name value",
        "description": "Description value",
        "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
        "certificate": "Y2VydGlmaWNhdGU="
      },
      "revokeOnUnenrollDisabled": true,
      "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
      "azureRightsManagementServicesAllowed": true,
      "iconsVisible": true,
      "protectedApps": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
          "displayName": "Display Name value",
          "description": "Description value",
          "publisherName": "Publisher Name value",
          "productName": "Product Name value",
          "denied": true
        }
      ],
      "exemptApps": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
          "displayName": "Display Name value",
          "description": "Description value",
          "publisherName": "Publisher Name value",
          "productName": "Product Name value",
          "denied": true
        }
      ],
      "enterpriseNetworkDomainNames": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "enterpriseProxiedDomains": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
          "displayName": "Display Name value",
          "proxiedDomains": [
            {
              "@odata.type": "microsoft.graph.proxiedDomain",
              "ipAddressOrFQDN": "Ip Address Or FQDN value",
              "proxy": "Proxy value"
            }
          ]
        }
      ],
      "enterpriseIPRanges": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
          "displayName": "Display Name value",
          "ranges": [
            {
              "@odata.type": "microsoft.graph.iPv6Range",
              "lowerAddress": "Lower Address value",
              "upperAddress": "Upper Address value"
            }
          ]
        }
      ],
      "enterpriseIPRangesAreAuthoritative": true,
      "enterpriseProxyServers": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "enterpriseInternalProxyServers": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "enterpriseProxyServersAreAuthoritative": true,
      "neutralDomainResources": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "indexingEncryptedStoresOrItemsBlocked": true,
      "smbAutoEncryptedFileExtensions": [
        {
          "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
          "displayName": "Display Name value",
          "resources": [
            "Resources value"
          ]
        }
      ],
      "isAssigned": true,
      "revokeOnMdmHandoffDisabled": true,
      "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
      "windowsHelloForBusinessBlocked": true,
      "pinMinimumLength": 0,
      "pinUppercaseLetters": "requireAtLeastOne",
      "pinLowercaseLetters": "requireAtLeastOne",
      "pinSpecialCharacters": "requireAtLeastOne",
      "pinExpirationDays": 1,
      "numberOfPastPinsRemembered": 10,
      "passwordMaximumAttemptCount": 11,
      "minutesOfInactivityBeforeDeviceLock": 3,
      "daysWithoutContactBeforeUnenroll": 0
    }
  ]
}
```


