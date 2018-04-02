# <a name="list-managedioslobapps"></a><span data-ttu-id="71253-101">managedIOSLobApps のリスト</span><span class="sxs-lookup"><span data-stu-id="71253-101">List managedIOSLobApps</span></span>

> <span data-ttu-id="71253-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="71253-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71253-103">[managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="71253-103">List properties and relationships of the [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71253-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="71253-104">Prerequisites</span></span>
<span data-ttu-id="71253-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71253-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="71253-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="71253-107">Permission type</span></span>|<span data-ttu-id="71253-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="71253-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71253-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="71253-109">Delegated (work or school account)</span></span>|<span data-ttu-id="71253-110">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="71253-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="71253-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="71253-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71253-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="71253-112">Not supported.</span></span>|
|<span data-ttu-id="71253-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="71253-113">Application</span></span>|<span data-ttu-id="71253-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="71253-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71253-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="71253-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="71253-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="71253-116">Request headers</span></span>
|<span data-ttu-id="71253-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="71253-117">Header</span></span>|<span data-ttu-id="71253-118">値</span><span class="sxs-lookup"><span data-stu-id="71253-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71253-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="71253-119">Authorization</span></span>|<span data-ttu-id="71253-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="71253-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="71253-121">Accept</span><span class="sxs-lookup"><span data-stu-id="71253-121">Accept</span></span>|<span data-ttu-id="71253-122">application/json</span><span class="sxs-lookup"><span data-stu-id="71253-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71253-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="71253-123">Request body</span></span>
<span data-ttu-id="71253-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="71253-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71253-125">応答</span><span class="sxs-lookup"><span data-stu-id="71253-125">Response</span></span>
<span data-ttu-id="71253-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="71253-126">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/intune_apps_managedioslobapp.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71253-127">例</span><span class="sxs-lookup"><span data-stu-id="71253-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="71253-128">要求</span><span class="sxs-lookup"><span data-stu-id="71253-128">Request</span></span>
<span data-ttu-id="71253-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="71253-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
```

### <a name="response"></a><span data-ttu-id="71253-130">応答</span><span class="sxs-lookup"><span data-stu-id="71253-130">Response</span></span>
<span data-ttu-id="71253-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="71253-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1632

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedIOSLobApp",
      "id": "8f59792d-792d-8f59-2d79-598f2d79598f",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisher": "Publisher value",
      "largeIcon": {
        "@odata.type": "microsoft.graph.mimeContent",
        "type": "Type value",
        "value": "dmFsdWU="
      },
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "isFeatured": true,
      "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
      "informationUrl": "https://example.com/informationUrl/",
      "owner": "Owner value",
      "developer": "Developer value",
      "notes": "Notes value",
      "publishingState": "processing",
      "appAvailability": "lineOfBusiness",
      "version": "Version value",
      "committedContentVersion": "Committed Content Version value",
      "fileName": "File Name value",
      "size": 4,
      "bundleId": "Bundle Id value",
      "applicableDeviceType": {
        "@odata.type": "microsoft.graph.iosDeviceType",
        "iPad": true,
        "iPhoneAndIPod": true
      },
      "minimumSupportedOperatingSystem": {
        "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
        "v8_0": true,
        "v9_0": true,
        "v10_0": true,
        "v11_0": true
      },
      "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
      "versionNumber": "Version Number value",
      "buildNumber": "Build Number value"
    }
  ]
}
```


