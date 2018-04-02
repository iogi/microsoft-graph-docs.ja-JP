# <a name="list-windowsinformationprotectionapplearningsummaries"></a><span data-ttu-id="78bc7-101">windowsInformationProtectionAppLearningSummaries のリスト</span><span class="sxs-lookup"><span data-stu-id="78bc7-101">List windowsInformationProtectionAppLearningSummaries</span></span>

> <span data-ttu-id="78bc7-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="78bc7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="78bc7-103">[windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="78bc7-103">List properties and relationships of the [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="78bc7-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="78bc7-104">Prerequisites</span></span>
<span data-ttu-id="78bc7-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78bc7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="78bc7-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="78bc7-107">Permission type</span></span>|<span data-ttu-id="78bc7-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="78bc7-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="78bc7-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="78bc7-109">Delegated (work or school account)</span></span>|<span data-ttu-id="78bc7-110">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="78bc7-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="78bc7-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="78bc7-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="78bc7-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="78bc7-112">Not supported.</span></span>|
|<span data-ttu-id="78bc7-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="78bc7-113">Application</span></span>|<span data-ttu-id="78bc7-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="78bc7-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="78bc7-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="78bc7-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/windowsInformationProtectionAppLearningSummaries
```

## <a name="request-headers"></a><span data-ttu-id="78bc7-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="78bc7-116">Request headers</span></span>
|<span data-ttu-id="78bc7-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="78bc7-117">Header</span></span>|<span data-ttu-id="78bc7-118">値</span><span class="sxs-lookup"><span data-stu-id="78bc7-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="78bc7-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="78bc7-119">Authorization</span></span>|<span data-ttu-id="78bc7-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="78bc7-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="78bc7-121">Accept</span><span class="sxs-lookup"><span data-stu-id="78bc7-121">Accept</span></span>|<span data-ttu-id="78bc7-122">application/json</span><span class="sxs-lookup"><span data-stu-id="78bc7-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="78bc7-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="78bc7-123">Request body</span></span>
<span data-ttu-id="78bc7-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="78bc7-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="78bc7-125">応答</span><span class="sxs-lookup"><span data-stu-id="78bc7-125">Response</span></span>
<span data-ttu-id="78bc7-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [windowsInformationProtectionAppLearningSummary](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="78bc7-126">If successful, this method returns a `200 OK` response code and collection of [workbookRangeView](../resources/intune_wip_windowsinformationprotectionapplearningsummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="78bc7-127">例</span><span class="sxs-lookup"><span data-stu-id="78bc7-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="78bc7-128">要求</span><span class="sxs-lookup"><span data-stu-id="78bc7-128">Request</span></span>
<span data-ttu-id="78bc7-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="78bc7-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/windowsInformationProtectionAppLearningSummaries
```

### <a name="response"></a><span data-ttu-id="78bc7-130">応答</span><span class="sxs-lookup"><span data-stu-id="78bc7-130">Response</span></span>
<span data-ttu-id="78bc7-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="78bc7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 293

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.windowsInformationProtectionAppLearningSummary",
      "id": "063baf50-af50-063b-50af-3b0650af3b06",
      "applicationName": "Application Name value",
      "applicationType": "desktop",
      "deviceCount": 11
    }
  ]
}
```


