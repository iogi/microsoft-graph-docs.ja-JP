# <a name="get-androidmanagedappregistration"></a><span data-ttu-id="24b09-101">Get androidManagedAppRegistration</span><span class="sxs-lookup"><span data-stu-id="24b09-101">Get androidManagedAppRegistration</span></span>

> <span data-ttu-id="24b09-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="24b09-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="24b09-103">[androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md) オブジェクトのプロパティとリレーションシップを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="24b09-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_mam_androidmanagedappregistration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="24b09-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="24b09-104">Prerequisites</span></span>
<span data-ttu-id="24b09-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24b09-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="24b09-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="24b09-107">Permission type</span></span>|<span data-ttu-id="24b09-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="24b09-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="24b09-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="24b09-109">Delegated (work or school account)</span></span>|<span data-ttu-id="24b09-110">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="24b09-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="24b09-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="24b09-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="24b09-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="24b09-112">Not supported.</span></span>|
|<span data-ttu-id="24b09-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="24b09-113">Application</span></span>|<span data-ttu-id="24b09-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="24b09-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="24b09-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="24b09-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="24b09-116">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="24b09-116">Optional query parameters</span></span>
<span data-ttu-id="24b09-117">このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](https://developer.microsoft.com/ja-JP/graph/docs/overview/query_parameters)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="24b09-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/ja-JP/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="24b09-118">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="24b09-118">Request headers</span></span>
|<span data-ttu-id="24b09-119">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="24b09-119">Header</span></span>|<span data-ttu-id="24b09-120">値</span><span class="sxs-lookup"><span data-stu-id="24b09-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="24b09-121">承認</span><span class="sxs-lookup"><span data-stu-id="24b09-121">Authorization</span></span>|<span data-ttu-id="24b09-122">ベアラー &lt;トークン&gt;が必須。</span><span class="sxs-lookup"><span data-stu-id="24b09-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="24b09-123">承諾</span><span class="sxs-lookup"><span data-stu-id="24b09-123">Accept</span></span>|<span data-ttu-id="24b09-124">application/json</span><span class="sxs-lookup"><span data-stu-id="24b09-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="24b09-125">要求本文</span><span class="sxs-lookup"><span data-stu-id="24b09-125">Request body</span></span>
<span data-ttu-id="24b09-126">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="24b09-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="24b09-127">応答</span><span class="sxs-lookup"><span data-stu-id="24b09-127">Response</span></span>
<span data-ttu-id="24b09-128">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [androidManagedAppRegistration](../resources/intune_mam_androidmanagedappregistration.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="24b09-128">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/intune_mam_androidmanagedappregistration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="24b09-129">例</span><span class="sxs-lookup"><span data-stu-id="24b09-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="24b09-130">要求</span><span class="sxs-lookup"><span data-stu-id="24b09-130">Request</span></span>
<span data-ttu-id="24b09-131">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="24b09-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}
```

### <a name="response"></a><span data-ttu-id="24b09-132">応答</span><span class="sxs-lookup"><span data-stu-id="24b09-132">Response</span></span>
<span data-ttu-id="24b09-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="24b09-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 810

{
  "value": {
    "@odata.type": "#microsoft.graph.androidManagedAppRegistration",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
    "applicationVersion": "Application Version value",
    "managementSdkVersion": "Management Sdk Version value",
    "platformVersion": "Platform Version value",
    "deviceType": "Device Type value",
    "deviceTag": "Device Tag value",
    "deviceName": "Device Name value",
    "flaggedReasons": [
      "rootedDevice"
    ],
    "userId": "User Id value",
    "appIdentifier": {
      "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
      "packageId": "Package Id value"
    },
    "id": "0e064997-4997-0e06-9749-060e9749060e",
    "version": "Version value"
  }
}
```


