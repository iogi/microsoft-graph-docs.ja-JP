# <a name="update-enrollmentconfigurationassignment"></a><span data-ttu-id="e7520-101">enrollmentConfigurationAssignment の更新</span><span class="sxs-lookup"><span data-stu-id="e7520-101">Update enrollmentConfigurationAssignment</span></span>

> <span data-ttu-id="e7520-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7520-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e7520-103">[enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="e7520-103">Update the properties of a [calendar](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e7520-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="e7520-104">Prerequisites</span></span>
<span data-ttu-id="e7520-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7520-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e7520-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="e7520-107">Permission type</span></span>|<span data-ttu-id="e7520-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="e7520-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e7520-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="e7520-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e7520-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e7520-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="e7520-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="e7520-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e7520-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e7520-112">Not supported.</span></span>|
|<span data-ttu-id="e7520-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="e7520-113">Application</span></span>|<span data-ttu-id="e7520-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e7520-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e7520-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="e7520-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments/{enrollmentConfigurationAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="e7520-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e7520-116">Request headers</span></span>
|<span data-ttu-id="e7520-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="e7520-117">Header</span></span>|<span data-ttu-id="e7520-118">値</span><span class="sxs-lookup"><span data-stu-id="e7520-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e7520-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e7520-119">Authorization</span></span>|<span data-ttu-id="e7520-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="e7520-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="e7520-121">Accept</span><span class="sxs-lookup"><span data-stu-id="e7520-121">Accept</span></span>|<span data-ttu-id="e7520-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e7520-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e7520-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="e7520-123">Request body</span></span>
<span data-ttu-id="e7520-124">要求本文で、[enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7520-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object.</span></span>

<span data-ttu-id="e7520-125">次の表に、[enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="e7520-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="e7520-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7520-126">Property</span></span>|<span data-ttu-id="e7520-127">型</span><span class="sxs-lookup"><span data-stu-id="e7520-127">Type</span></span>|<span data-ttu-id="e7520-128">説明</span><span class="sxs-lookup"><span data-stu-id="e7520-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e7520-129">id</span><span class="sxs-lookup"><span data-stu-id="e7520-129">id</span></span>|<span data-ttu-id="e7520-130">String</span><span class="sxs-lookup"><span data-stu-id="e7520-130">String</span></span>|<span data-ttu-id="e7520-131">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="e7520-131">Not yet documented</span></span>|
|<span data-ttu-id="e7520-132">target</span><span class="sxs-lookup"><span data-stu-id="e7520-132">target</span></span>|[<span data-ttu-id="e7520-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="e7520-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_onboarding_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="e7520-134">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="e7520-134">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="e7520-135">応答</span><span class="sxs-lookup"><span data-stu-id="e7520-135">Response</span></span>
<span data-ttu-id="e7520-136">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [enrollmentConfigurationAssignment](../resources/intune_onboarding_enrollmentconfigurationassignment.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="e7520-136">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_onboarding_enrollmentconfigurationassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e7520-137">例</span><span class="sxs-lookup"><span data-stu-id="e7520-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="e7520-138">要求</span><span class="sxs-lookup"><span data-stu-id="e7520-138">Request</span></span>
<span data-ttu-id="e7520-139">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="e7520-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}/assignments/{enrollmentConfigurationAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="e7520-140">応答</span><span class="sxs-lookup"><span data-stu-id="e7520-140">Response</span></span>
<span data-ttu-id="e7520-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="e7520-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 222

{
  "@odata.type": "#microsoft.graph.enrollmentConfigurationAssignment",
  "id": "705b021c-021c-705b-1c02-5b701c025b70",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```


