# <a name="create-devicemanagementpartner"></a><span data-ttu-id="b3e2c-101">deviceManagementPartner の作成</span><span class="sxs-lookup"><span data-stu-id="b3e2c-101">Create deviceManagementPartner</span></span>

> <span data-ttu-id="b3e2c-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3e2c-103">新しい [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-103">Create a new [plannerBucket](../resources/intune_onboarding_devicemanagementpartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3e2c-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="b3e2c-104">Prerequisites</span></span>
<span data-ttu-id="b3e2c-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b3e2c-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="b3e2c-107">Permission type</span></span>|<span data-ttu-id="b3e2c-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="b3e2c-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3e2c-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="b3e2c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b3e2c-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b3e2c-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="b3e2c-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="b3e2c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3e2c-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-112">Not supported.</span></span>|
|<span data-ttu-id="b3e2c-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b3e2c-113">Application</span></span>|<span data-ttu-id="b3e2c-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3e2c-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="b3e2c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceManagementPartners
```

## <a name="request-headers"></a><span data-ttu-id="b3e2c-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b3e2c-116">Request headers</span></span>
|<span data-ttu-id="b3e2c-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b3e2c-117">Header</span></span>|<span data-ttu-id="b3e2c-118">値</span><span class="sxs-lookup"><span data-stu-id="b3e2c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3e2c-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="b3e2c-119">Authorization</span></span>|<span data-ttu-id="b3e2c-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="b3e2c-121">Accept</span><span class="sxs-lookup"><span data-stu-id="b3e2c-121">Accept</span></span>|<span data-ttu-id="b3e2c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b3e2c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3e2c-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="b3e2c-123">Request body</span></span>
<span data-ttu-id="b3e2c-124">要求本文で、deviceManagementPartner オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="b3e2c-125">次の表に、deviceManagementPartner の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="b3e2c-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b3e2c-126">Property</span></span>|<span data-ttu-id="b3e2c-127">型</span><span class="sxs-lookup"><span data-stu-id="b3e2c-127">Type</span></span>|<span data-ttu-id="b3e2c-128">説明</span><span class="sxs-lookup"><span data-stu-id="b3e2c-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3e2c-129">id</span><span class="sxs-lookup"><span data-stu-id="b3e2c-129">id</span></span>|<span data-ttu-id="b3e2c-130">String</span><span class="sxs-lookup"><span data-stu-id="b3e2c-130">String</span></span>|<span data-ttu-id="b3e2c-131">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="b3e2c-131">Not yet documented</span></span>|
|<span data-ttu-id="b3e2c-132">lastHeartbeatDateTime</span><span class="sxs-lookup"><span data-stu-id="b3e2c-132">lastHeartbeatDateTime</span></span>|<span data-ttu-id="b3e2c-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3e2c-133">DateTimeOffset</span></span>|<span data-ttu-id="b3e2c-134">管理者が [デバイス管理パートナーに接続] オプションを有効にした後の最終ハートビートのタイムスタンプ</span><span class="sxs-lookup"><span data-stu-id="b3e2c-134">Timestamp of last heartbeat after admin enabled option Connect to Device management Partner</span></span>|
|<span data-ttu-id="b3e2c-135">partnerState</span><span class="sxs-lookup"><span data-stu-id="b3e2c-135">partnerState</span></span>|<span data-ttu-id="b3e2c-136">String</span><span class="sxs-lookup"><span data-stu-id="b3e2c-136">String</span></span>|<span data-ttu-id="b3e2c-137">このテナントのパートナーの状態。可能な値は、`unknown`、`unavailable`、`enabled`、`terminated`、`rejected`、`unresponsive` です。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-137">Partner state of this tenant Possible values are: `unknown`, `unavailable`, `enabled`, `terminated`, `rejected`, `unresponsive`.</span></span>|
|<span data-ttu-id="b3e2c-138">partnerAppType</span><span class="sxs-lookup"><span data-stu-id="b3e2c-138">partnerAppType</span></span>|<span data-ttu-id="b3e2c-139">String</span><span class="sxs-lookup"><span data-stu-id="b3e2c-139">String</span></span>|<span data-ttu-id="b3e2c-140">パートナー アプリの種類。可能な値は、`unknown`、`singleTenantApp`、`multiTenantApp` です。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-140">Partner App type Possible values are: `unknown`, `singleTenantApp`, `multiTenantApp`.</span></span>|
|<span data-ttu-id="b3e2c-141">singleTenantAppId</span><span class="sxs-lookup"><span data-stu-id="b3e2c-141">singleTenantAppId</span></span>|<span data-ttu-id="b3e2c-142">String</span><span class="sxs-lookup"><span data-stu-id="b3e2c-142">String</span></span>|<span data-ttu-id="b3e2c-143">パートナーのシングル テナントのアプリ ID</span><span class="sxs-lookup"><span data-stu-id="b3e2c-143">Partner Single tenant App id</span></span>|
|<span data-ttu-id="b3e2c-144">displayName</span><span class="sxs-lookup"><span data-stu-id="b3e2c-144">displayName</span></span>|<span data-ttu-id="b3e2c-145">String</span><span class="sxs-lookup"><span data-stu-id="b3e2c-145">String</span></span>|<span data-ttu-id="b3e2c-146">パートナー表示名</span><span class="sxs-lookup"><span data-stu-id="b3e2c-146">Partner display name</span></span>|
|<span data-ttu-id="b3e2c-147">isConfigured</span><span class="sxs-lookup"><span data-stu-id="b3e2c-147">isConfigured</span></span>|<span data-ttu-id="b3e2c-148">Boolean</span><span class="sxs-lookup"><span data-stu-id="b3e2c-148">Boolean</span></span>|<span data-ttu-id="b3e2c-149">デバイス管理パートナーが構成されているかどうか</span><span class="sxs-lookup"><span data-stu-id="b3e2c-149">Whether device management partner is configured or not</span></span>|
|<span data-ttu-id="b3e2c-150">whenPartnerDevicesWillBeRemovedDateTime</span><span class="sxs-lookup"><span data-stu-id="b3e2c-150">whenPartnerDevicesWillBeRemovedDateTime</span></span>|<span data-ttu-id="b3e2c-151">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3e2c-151">DateTimeOffset</span></span>|<span data-ttu-id="b3e2c-152">パートナー デバイスが削除される日時 (UTC)</span><span class="sxs-lookup"><span data-stu-id="b3e2c-152">DateTime in UTC when PartnerDevices will be removed</span></span>|
|<span data-ttu-id="b3e2c-153">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span><span class="sxs-lookup"><span data-stu-id="b3e2c-153">whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime</span></span>|<span data-ttu-id="b3e2c-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b3e2c-154">DateTimeOffset</span></span>|<span data-ttu-id="b3e2c-155">パートナー デバイスが準拠していないとマークされる日時 (UTC)</span><span class="sxs-lookup"><span data-stu-id="b3e2c-155">DateTime in UTC when PartnerDevices will be marked as NonCompliant</span></span>|



## <a name="response"></a><span data-ttu-id="b3e2c-156">応答</span><span class="sxs-lookup"><span data-stu-id="b3e2c-156">Response</span></span>
<span data-ttu-id="b3e2c-157">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [deviceManagementPartner](../resources/intune_onboarding_devicemanagementpartner.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-157">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_onboarding_devicemanagementpartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3e2c-158">例</span><span class="sxs-lookup"><span data-stu-id="b3e2c-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3e2c-159">要求</span><span class="sxs-lookup"><span data-stu-id="b3e2c-159">Request</span></span>
<span data-ttu-id="b3e2c-160">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-160">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceManagementPartners
Content-type: application/json
Content-length: 502

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```

### <a name="response"></a><span data-ttu-id="b3e2c-161">応答</span><span class="sxs-lookup"><span data-stu-id="b3e2c-161">Response</span></span>
<span data-ttu-id="b3e2c-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="b3e2c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 551

{
  "@odata.type": "#microsoft.graph.deviceManagementPartner",
  "id": "d21e377a-377a-d21e-7a37-1ed27a371ed2",
  "lastHeartbeatDateTime": "2016-12-31T23:59:37.9174975-08:00",
  "partnerState": "unavailable",
  "partnerAppType": "singleTenantApp",
  "singleTenantAppId": "Single Tenant App Id value",
  "displayName": "Display Name value",
  "isConfigured": true,
  "whenPartnerDevicesWillBeRemovedDateTime": "2016-12-31T23:56:38.2655023-08:00",
  "whenPartnerDevicesWillBeMarkedAsNonCompliantDateTime": "2016-12-31T23:58:42.2131231-08:00"
}
```


