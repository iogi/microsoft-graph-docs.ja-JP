# <a name="update-devicemanagement"></a><span data-ttu-id="f044a-101">deviceManagement の更新</span><span class="sxs-lookup"><span data-stu-id="f044a-101">Update deviceManagement</span></span>

> <span data-ttu-id="f044a-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f044a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f044a-103">[deviceManagement](../resources/intune_corpenrollment_devicemanagement.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="f044a-103">Update the properties of a [calendar](../resources/intune_corpenrollment_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f044a-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="f044a-104">Prerequisites</span></span>
<span data-ttu-id="f044a-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f044a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f044a-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="f044a-107">Permission type</span></span>|<span data-ttu-id="f044a-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="f044a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f044a-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="f044a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f044a-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f044a-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f044a-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="f044a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f044a-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f044a-112">Not supported.</span></span>|
|<span data-ttu-id="f044a-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f044a-113">Application</span></span>|<span data-ttu-id="f044a-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f044a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f044a-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="f044a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement
```

## <a name="request-headers"></a><span data-ttu-id="f044a-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f044a-116">Request headers</span></span>
|<span data-ttu-id="f044a-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f044a-117">Header</span></span>|<span data-ttu-id="f044a-118">値</span><span class="sxs-lookup"><span data-stu-id="f044a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f044a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f044a-119">Authorization</span></span>|<span data-ttu-id="f044a-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="f044a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="f044a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="f044a-121">Accept</span></span>|<span data-ttu-id="f044a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f044a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f044a-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="f044a-123">Request body</span></span>
<span data-ttu-id="f044a-124">要求本文で、[deviceManagement](../resources/intune_corpenrollment_devicemanagement.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="f044a-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_corpenrollment_devicemanagement.md) object.</span></span>

<span data-ttu-id="f044a-125">次の表に、[deviceManagement](../resources/intune_corpenrollment_devicemanagement.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="f044a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="f044a-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f044a-126">Property</span></span>|<span data-ttu-id="f044a-127">型</span><span class="sxs-lookup"><span data-stu-id="f044a-127">Type</span></span>|<span data-ttu-id="f044a-128">説明</span><span class="sxs-lookup"><span data-stu-id="f044a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f044a-129">id</span><span class="sxs-lookup"><span data-stu-id="f044a-129">id</span></span>|<span data-ttu-id="f044a-130">String</span><span class="sxs-lookup"><span data-stu-id="f044a-130">String</span></span>|<span data-ttu-id="f044a-131">オブジェクトの GUID。</span><span class="sxs-lookup"><span data-stu-id="f044a-131">The user GUID for the security object is not valid.</span></span>|



## <a name="response"></a><span data-ttu-id="f044a-132">応答</span><span class="sxs-lookup"><span data-stu-id="f044a-132">Response</span></span>
<span data-ttu-id="f044a-133">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [deviceManagement](../resources/intune_corpenrollment_devicemanagement.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="f044a-133">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_corpenrollment_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f044a-134">例</span><span class="sxs-lookup"><span data-stu-id="f044a-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="f044a-135">要求</span><span class="sxs-lookup"><span data-stu-id="f044a-135">Request</span></span>
<span data-ttu-id="f044a-136">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="f044a-136">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="f044a-137">応答</span><span class="sxs-lookup"><span data-stu-id="f044a-137">Response</span></span>
<span data-ttu-id="f044a-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="f044a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 107

{
  "@odata.type": "#microsoft.graph.deviceManagement",
  "id": "0b283420-3420-0b28-2034-280b2034280b"
}
```


