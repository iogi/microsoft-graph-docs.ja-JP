# <a name="update-devicemanagementtroubleshootingevent"></a><span data-ttu-id="537ac-101">deviceManagementTroubleshootingEvent の更新</span><span class="sxs-lookup"><span data-stu-id="537ac-101">Update deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="537ac-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="537ac-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="537ac-103">[deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="537ac-103">Update the properties of a [calendar](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="537ac-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="537ac-104">Prerequisites</span></span>
<span data-ttu-id="537ac-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="537ac-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="537ac-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="537ac-107">Permission type</span></span>|<span data-ttu-id="537ac-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="537ac-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="537ac-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="537ac-109">Delegated (work or school account)</span></span>|<span data-ttu-id="537ac-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="537ac-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="537ac-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="537ac-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="537ac-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="537ac-112">Not supported.</span></span>|
|<span data-ttu-id="537ac-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="537ac-113">Application</span></span>|<span data-ttu-id="537ac-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="537ac-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="537ac-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="537ac-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="537ac-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="537ac-116">Request headers</span></span>
|<span data-ttu-id="537ac-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="537ac-117">Header</span></span>|<span data-ttu-id="537ac-118">値</span><span class="sxs-lookup"><span data-stu-id="537ac-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="537ac-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="537ac-119">Authorization</span></span>|<span data-ttu-id="537ac-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="537ac-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="537ac-121">Accept</span><span class="sxs-lookup"><span data-stu-id="537ac-121">Accept</span></span>|<span data-ttu-id="537ac-122">application/json</span><span class="sxs-lookup"><span data-stu-id="537ac-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="537ac-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="537ac-123">Request body</span></span>
<span data-ttu-id="537ac-124">要求本文で、[deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="537ac-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object.</span></span>

<span data-ttu-id="537ac-125">次の表に、[deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="537ac-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="537ac-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="537ac-126">Property</span></span>|<span data-ttu-id="537ac-127">型</span><span class="sxs-lookup"><span data-stu-id="537ac-127">Type</span></span>|<span data-ttu-id="537ac-128">説明</span><span class="sxs-lookup"><span data-stu-id="537ac-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="537ac-129">id</span><span class="sxs-lookup"><span data-stu-id="537ac-129">id</span></span>|<span data-ttu-id="537ac-130">String</span><span class="sxs-lookup"><span data-stu-id="537ac-130">String</span></span>|<span data-ttu-id="537ac-131">オブジェクトの UUID</span><span class="sxs-lookup"><span data-stu-id="537ac-131">UUID for the object</span></span>|
|<span data-ttu-id="537ac-132">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="537ac-132">eventDateTime</span></span>|<span data-ttu-id="537ac-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="537ac-133">DateTimeOffset</span></span>|<span data-ttu-id="537ac-134">イベントが発生した時刻。</span><span class="sxs-lookup"><span data-stu-id="537ac-134">Time when the event occurred .</span></span>|
|<span data-ttu-id="537ac-135">correlationId</span><span class="sxs-lookup"><span data-stu-id="537ac-135">correlation_id</span></span>|<span data-ttu-id="537ac-136">String</span><span class="sxs-lookup"><span data-stu-id="537ac-136">String</span></span>|<span data-ttu-id="537ac-137">サービスのエラーをトレースするための ID。</span><span class="sxs-lookup"><span data-stu-id="537ac-137">Id used for tracing the failure in the service.</span></span>|



## <a name="response"></a><span data-ttu-id="537ac-138">応答</span><span class="sxs-lookup"><span data-stu-id="537ac-138">Response</span></span>
<span data-ttu-id="537ac-139">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="537ac-139">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="537ac-140">例</span><span class="sxs-lookup"><span data-stu-id="537ac-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="537ac-141">要求</span><span class="sxs-lookup"><span data-stu-id="537ac-141">Request</span></span>
<span data-ttu-id="537ac-142">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="537ac-142">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
Content-type: application/json
Content-length: 104

{
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```

### <a name="response"></a><span data-ttu-id="537ac-143">応答</span><span class="sxs-lookup"><span data-stu-id="537ac-143">Response</span></span>
<span data-ttu-id="537ac-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="537ac-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
  "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```


