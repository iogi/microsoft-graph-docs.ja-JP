# <a name="list-macosdevicefeaturesconfigurations"></a><span data-ttu-id="07b3a-101">macOSDeviceFeaturesConfigurations のリスト</span><span class="sxs-lookup"><span data-stu-id="07b3a-101">List macOSDeviceFeaturesConfigurations</span></span>

> <span data-ttu-id="07b3a-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="07b3a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="07b3a-103">[macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="07b3a-103">List properties and relationships of the [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="07b3a-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="07b3a-104">Prerequisites</span></span>
<span data-ttu-id="07b3a-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07b3a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="07b3a-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="07b3a-107">Permission type</span></span>|<span data-ttu-id="07b3a-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="07b3a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="07b3a-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="07b3a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="07b3a-110">DeviceManagementConfiguration.ReadWrite.All、DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="07b3a-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="07b3a-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="07b3a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="07b3a-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="07b3a-112">Not supported.</span></span>|
|<span data-ttu-id="07b3a-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="07b3a-113">Application</span></span>|<span data-ttu-id="07b3a-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="07b3a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="07b3a-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="07b3a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="07b3a-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="07b3a-116">Request headers</span></span>
|<span data-ttu-id="07b3a-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="07b3a-117">Header</span></span>|<span data-ttu-id="07b3a-118">値</span><span class="sxs-lookup"><span data-stu-id="07b3a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="07b3a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="07b3a-119">Authorization</span></span>|<span data-ttu-id="07b3a-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="07b3a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="07b3a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="07b3a-121">Accept</span></span>|<span data-ttu-id="07b3a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="07b3a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="07b3a-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="07b3a-123">Request body</span></span>
<span data-ttu-id="07b3a-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="07b3a-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="07b3a-125">応答</span><span class="sxs-lookup"><span data-stu-id="07b3a-125">Response</span></span>
<span data-ttu-id="07b3a-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="07b3a-126">If successful, this method returns a `200 OK` response code and collection of [workbookRangeView](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="07b3a-127">例</span><span class="sxs-lookup"><span data-stu-id="07b3a-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="07b3a-128">要求</span><span class="sxs-lookup"><span data-stu-id="07b3a-128">Request</span></span>
<span data-ttu-id="07b3a-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="07b3a-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="07b3a-130">応答</span><span class="sxs-lookup"><span data-stu-id="07b3a-130">Response</span></span>
<span data-ttu-id="07b3a-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="07b3a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 403

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
      "id": "49fa957d-957d-49fa-7d95-fa497d95fa49",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7
    }
  ]
}
```


