# <a name="get-managedapppolicydeploymentsummary"></a><span data-ttu-id="1c677-101">managedAppPolicyDeploymentSummary の取得</span><span class="sxs-lookup"><span data-stu-id="1c677-101">Get managedAppPolicyDeploymentSummary</span></span>

> <span data-ttu-id="1c677-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c677-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1c677-103">[managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) オブジェクトのプロパティとリレーションシップを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="1c677-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_mam_managedapppolicydeploymentsummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1c677-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="1c677-104">Prerequisites</span></span>
<span data-ttu-id="1c677-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c677-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1c677-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="1c677-107">Permission type</span></span>|<span data-ttu-id="1c677-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="1c677-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1c677-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="1c677-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1c677-110">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="1c677-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="1c677-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="1c677-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1c677-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c677-112">Not supported.</span></span>|
|<span data-ttu-id="1c677-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="1c677-113">Application</span></span>|<span data-ttu-id="1c677-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1c677-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1c677-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="1c677-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
GET /deviceAppManagement/androidManagedAppProtections/{androidManagedAppProtectionId}/deploymentSummary
GET /deviceAppManagement/defaultManagedAppProtections/{defaultManagedAppProtectionId}/deploymentSummary
GET /deviceAppManagement/targetedManagedAppConfigurations/{targetedManagedAppConfigurationId}/deploymentSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="1c677-116">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c677-116">Optional query parameters</span></span>
<span data-ttu-id="1c677-117">このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](https://developer.microsoft.com/ja-JP/graph/docs/overview/query_parameters)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="1c677-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/ja-JP/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1c677-118">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="1c677-118">Request headers</span></span>
|<span data-ttu-id="1c677-119">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="1c677-119">Header</span></span>|<span data-ttu-id="1c677-120">値</span><span class="sxs-lookup"><span data-stu-id="1c677-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1c677-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c677-121">Authorization</span></span>|<span data-ttu-id="1c677-122">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="1c677-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="1c677-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1c677-123">Accept</span></span>|<span data-ttu-id="1c677-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1c677-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1c677-125">要求本文</span><span class="sxs-lookup"><span data-stu-id="1c677-125">Request body</span></span>
<span data-ttu-id="1c677-126">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="1c677-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c677-127">応答</span><span class="sxs-lookup"><span data-stu-id="1c677-127">Response</span></span>
<span data-ttu-id="1c677-128">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [managedAppPolicyDeploymentSummary](../resources/intune_mam_managedapppolicydeploymentsummary.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="1c677-128">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/intune_mam_managedapppolicydeploymentsummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c677-129">例</span><span class="sxs-lookup"><span data-stu-id="1c677-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1c677-130">要求</span><span class="sxs-lookup"><span data-stu-id="1c677-130">Request</span></span>
<span data-ttu-id="1c677-131">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="1c677-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/iosManagedAppProtections/{iosManagedAppProtectionId}/deploymentSummary
```

### <a name="response"></a><span data-ttu-id="1c677-132">応答</span><span class="sxs-lookup"><span data-stu-id="1c677-132">Response</span></span>
<span data-ttu-id="1c677-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="1c677-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 688

{
  "value": {
    "@odata.type": "#microsoft.graph.managedAppPolicyDeploymentSummary",
    "displayName": "Display Name value",
    "configurationDeployedUserCount": 14,
    "lastRefreshTime": "2017-01-01T00:01:30.1240368-08:00",
    "configurationDeploymentSummaryPerApp": [
      {
        "@odata.type": "microsoft.graph.managedAppPolicyDeploymentSummaryPerApp",
        "mobileAppIdentifier": {
          "@odata.type": "microsoft.graph.androidMobileAppIdentifier",
          "packageId": "Package Id value"
        },
        "configurationAppliedUserCount": 13
      }
    ],
    "id": "61f2f688-f688-61f2-88f6-f26188f6f261",
    "version": "Version value"
  }
}
```


