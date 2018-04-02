# <a name="create-deviceinstallstate"></a><span data-ttu-id="33a11-101">deviceInstallState の作成</span><span class="sxs-lookup"><span data-stu-id="33a11-101">Create deviceInstallState</span></span>

> <span data-ttu-id="33a11-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="33a11-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="33a11-103">新しい [deviceInstallState](../resources/intune_books_deviceinstallstate.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="33a11-103">Create a new [plannerBucket](../resources/intune_books_deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="33a11-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="33a11-104">Prerequisites</span></span>
<span data-ttu-id="33a11-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33a11-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="33a11-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="33a11-107">Permission type</span></span>|<span data-ttu-id="33a11-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="33a11-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="33a11-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="33a11-109">Delegated (work or school account)</span></span>|<span data-ttu-id="33a11-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="33a11-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="33a11-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="33a11-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="33a11-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="33a11-112">Not supported.</span></span>|
|<span data-ttu-id="33a11-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="33a11-113">Application</span></span>|<span data-ttu-id="33a11-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="33a11-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="33a11-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="33a11-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="33a11-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="33a11-116">Request headers</span></span>
|<span data-ttu-id="33a11-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="33a11-117">Header</span></span>|<span data-ttu-id="33a11-118">値</span><span class="sxs-lookup"><span data-stu-id="33a11-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="33a11-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="33a11-119">Authorization</span></span>|<span data-ttu-id="33a11-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="33a11-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="33a11-121">Accept</span><span class="sxs-lookup"><span data-stu-id="33a11-121">Accept</span></span>|<span data-ttu-id="33a11-122">application/json</span><span class="sxs-lookup"><span data-stu-id="33a11-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="33a11-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="33a11-123">Request body</span></span>
<span data-ttu-id="33a11-124">要求本文で、deviceInstallState オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="33a11-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="33a11-125">次の表に、deviceInstallState の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="33a11-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="33a11-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="33a11-126">Property</span></span>|<span data-ttu-id="33a11-127">型</span><span class="sxs-lookup"><span data-stu-id="33a11-127">Type</span></span>|<span data-ttu-id="33a11-128">説明</span><span class="sxs-lookup"><span data-stu-id="33a11-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="33a11-129">id</span><span class="sxs-lookup"><span data-stu-id="33a11-129">id</span></span>|<span data-ttu-id="33a11-130">String</span><span class="sxs-lookup"><span data-stu-id="33a11-130">String</span></span>|<span data-ttu-id="33a11-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="33a11-131">Name of the entity.</span></span>|
|<span data-ttu-id="33a11-132">deviceName</span><span class="sxs-lookup"><span data-stu-id="33a11-132">DeviceName</span></span>|<span data-ttu-id="33a11-133">String</span><span class="sxs-lookup"><span data-stu-id="33a11-133">String</span></span>|<span data-ttu-id="33a11-134">デバイス名。</span><span class="sxs-lookup"><span data-stu-id="33a11-134">Device name.</span></span>|
|<span data-ttu-id="33a11-135">deviceId</span><span class="sxs-lookup"><span data-stu-id="33a11-135">deviceId</span></span>|<span data-ttu-id="33a11-136">String</span><span class="sxs-lookup"><span data-stu-id="33a11-136">String</span></span>|<span data-ttu-id="33a11-137">デバイス ID。</span><span class="sxs-lookup"><span data-stu-id="33a11-137">Device Id.</span></span>|
|<span data-ttu-id="33a11-138">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="33a11-138">lastSyncDateTime</span></span>|<span data-ttu-id="33a11-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="33a11-139">DateTimeOffset</span></span>|<span data-ttu-id="33a11-140">最後の同期日時。</span><span class="sxs-lookup"><span data-stu-id="33a11-140">Last sync date and time.</span></span>|
|<span data-ttu-id="33a11-141">installState</span><span class="sxs-lookup"><span data-stu-id="33a11-141">installState</span></span>|<span data-ttu-id="33a11-142">String</span><span class="sxs-lookup"><span data-stu-id="33a11-142">String</span></span>|<span data-ttu-id="33a11-143">電子ブックのインストールの状態。</span><span class="sxs-lookup"><span data-stu-id="33a11-143">The install state of the eBook.</span></span> <span data-ttu-id="33a11-144">可能な値は、`notApplicable`、`installed`、`failed`、`notInstalled`、`uninstallFailed`、`unknown` です。</span><span class="sxs-lookup"><span data-stu-id="33a11-144">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="33a11-145">errorCode</span><span class="sxs-lookup"><span data-stu-id="33a11-145">errorCode</span></span>|<span data-ttu-id="33a11-146">String</span><span class="sxs-lookup"><span data-stu-id="33a11-146">String</span></span>|<span data-ttu-id="33a11-147">インストール失敗のエラー コード。</span><span class="sxs-lookup"><span data-stu-id="33a11-147">The error code for install failures.</span></span>|
|<span data-ttu-id="33a11-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="33a11-148">osVersion</span></span>|<span data-ttu-id="33a11-149">String</span><span class="sxs-lookup"><span data-stu-id="33a11-149">String</span></span>|<span data-ttu-id="33a11-150">OS バージョン。</span><span class="sxs-lookup"><span data-stu-id="33a11-150">OS Version.</span></span>|
|<span data-ttu-id="33a11-151">osDescription</span><span class="sxs-lookup"><span data-stu-id="33a11-151">osDescription</span></span>|<span data-ttu-id="33a11-152">String</span><span class="sxs-lookup"><span data-stu-id="33a11-152">String</span></span>|<span data-ttu-id="33a11-153">OS の説明。</span><span class="sxs-lookup"><span data-stu-id="33a11-153">OS Description.</span></span>|
|<span data-ttu-id="33a11-154">userName</span><span class="sxs-lookup"><span data-stu-id="33a11-154">Username</span></span>|<span data-ttu-id="33a11-155">String</span><span class="sxs-lookup"><span data-stu-id="33a11-155">String</span></span>|<span data-ttu-id="33a11-156">デバイスのユーザー名。</span><span class="sxs-lookup"><span data-stu-id="33a11-156">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="33a11-157">応答</span><span class="sxs-lookup"><span data-stu-id="33a11-157">Response</span></span>
<span data-ttu-id="33a11-158">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [deviceInstallState](../resources/intune_books_deviceinstallstate.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="33a11-158">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_books_deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="33a11-159">例</span><span class="sxs-lookup"><span data-stu-id="33a11-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="33a11-160">要求</span><span class="sxs-lookup"><span data-stu-id="33a11-160">Request</span></span>
<span data-ttu-id="33a11-161">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="33a11-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
Content-type: application/json
Content-length: 374

{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "installState": "installed",
  "errorCode": "Error Code value",
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value"
}
```

### <a name="response"></a><span data-ttu-id="33a11-162">応答</span><span class="sxs-lookup"><span data-stu-id="33a11-162">Response</span></span>
<span data-ttu-id="33a11-p103">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="33a11-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 423

{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "b9feb68f-b68f-b9fe-8fb6-feb98fb6feb9",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "installState": "installed",
  "errorCode": "Error Code value",
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value"
}
```


