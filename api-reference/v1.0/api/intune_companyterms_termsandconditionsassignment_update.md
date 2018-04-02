# <a name="update-termsandconditionsassignment"></a><span data-ttu-id="f298e-101">termsAndConditionsAssignment の更新</span><span class="sxs-lookup"><span data-stu-id="f298e-101">Update termsAndConditionsAssignment</span></span>

> <span data-ttu-id="f298e-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f298e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f298e-103">[termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="f298e-103">Update the properties of a [calendar](../resources/intune_companyterms_termsandconditionsassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f298e-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="f298e-104">Prerequisites</span></span>
<span data-ttu-id="f298e-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f298e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f298e-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="f298e-107">Permission type</span></span>|<span data-ttu-id="f298e-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="f298e-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f298e-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="f298e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f298e-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f298e-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f298e-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="f298e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f298e-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f298e-112">Not supported.</span></span>|
|<span data-ttu-id="f298e-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f298e-113">Application</span></span>|<span data-ttu-id="f298e-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f298e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f298e-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="f298e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="f298e-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f298e-116">Request headers</span></span>
|<span data-ttu-id="f298e-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f298e-117">Header</span></span>|<span data-ttu-id="f298e-118">値</span><span class="sxs-lookup"><span data-stu-id="f298e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f298e-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f298e-119">Authorization</span></span>|<span data-ttu-id="f298e-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="f298e-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="f298e-121">Accept</span><span class="sxs-lookup"><span data-stu-id="f298e-121">Accept</span></span>|<span data-ttu-id="f298e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f298e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f298e-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="f298e-123">Request body</span></span>
<span data-ttu-id="f298e-124">要求本文で、[termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="f298e-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_companyterms_termsandconditionsassignment.md) object.</span></span>

<span data-ttu-id="f298e-125">次の表に、[termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="f298e-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="f298e-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f298e-126">Property</span></span>|<span data-ttu-id="f298e-127">型</span><span class="sxs-lookup"><span data-stu-id="f298e-127">Type</span></span>|<span data-ttu-id="f298e-128">説明</span><span class="sxs-lookup"><span data-stu-id="f298e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f298e-129">id</span><span class="sxs-lookup"><span data-stu-id="f298e-129">id</span></span>|<span data-ttu-id="f298e-130">String</span><span class="sxs-lookup"><span data-stu-id="f298e-130">String</span></span>|<span data-ttu-id="f298e-131">エンティティの一意識別子。</span><span class="sxs-lookup"><span data-stu-id="f298e-131">Unique identifier of the folder.</span></span>|
|<span data-ttu-id="f298e-132">target</span><span class="sxs-lookup"><span data-stu-id="f298e-132">target</span></span>|[<span data-ttu-id="f298e-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="f298e-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_companyterms_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="f298e-134">T & C ポリシーが割り当てられる、割り当て先です。</span><span class="sxs-lookup"><span data-stu-id="f298e-134">Assignment target that the T&C policy is assigned to.</span></span>|



## <a name="response"></a><span data-ttu-id="f298e-135">応答</span><span class="sxs-lookup"><span data-stu-id="f298e-135">Response</span></span>
<span data-ttu-id="f298e-136">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [termsAndConditionsAssignment](../resources/intune_companyterms_termsandconditionsassignment.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="f298e-136">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_companyterms_termsandconditionsassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f298e-137">例</span><span class="sxs-lookup"><span data-stu-id="f298e-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="f298e-138">要求</span><span class="sxs-lookup"><span data-stu-id="f298e-138">Request</span></span>
<span data-ttu-id="f298e-139">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="f298e-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/assignments/{termsAndConditionsAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="f298e-140">応答</span><span class="sxs-lookup"><span data-stu-id="f298e-140">Response</span></span>
<span data-ttu-id="f298e-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="f298e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 217

{
  "@odata.type": "#microsoft.graph.termsAndConditionsAssignment",
  "id": "64c1a196-a196-64c1-96a1-c16496a1c164",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```


