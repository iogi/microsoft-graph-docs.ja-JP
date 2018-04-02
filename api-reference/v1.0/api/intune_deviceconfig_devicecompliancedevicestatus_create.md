# <a name="create-devicecompliancedevicestatus"></a><span data-ttu-id="13d5a-101">deviceComplianceDeviceStatus の作成</span><span class="sxs-lookup"><span data-stu-id="13d5a-101">Create deviceComplianceDeviceStatus</span></span>

> <span data-ttu-id="13d5a-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="13d5a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="13d5a-103">新しい [deviceComplianceDeviceStatus](../resources/intune_deviceconfig_devicecompliancedevicestatus.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="13d5a-103">Create a new [plannerBucket](../resources/intune_deviceconfig_devicecompliancedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="13d5a-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="13d5a-104">Prerequisites</span></span>
<span data-ttu-id="13d5a-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13d5a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="13d5a-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="13d5a-107">Permission type</span></span>|<span data-ttu-id="13d5a-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="13d5a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="13d5a-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="13d5a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="13d5a-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="13d5a-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="13d5a-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="13d5a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="13d5a-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="13d5a-112">Not supported.</span></span>|
|<span data-ttu-id="13d5a-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="13d5a-113">Application</span></span>|<span data-ttu-id="13d5a-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="13d5a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="13d5a-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="13d5a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="13d5a-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="13d5a-116">Request headers</span></span>
|<span data-ttu-id="13d5a-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="13d5a-117">Header</span></span>|<span data-ttu-id="13d5a-118">値</span><span class="sxs-lookup"><span data-stu-id="13d5a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="13d5a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="13d5a-119">Authorization</span></span>|<span data-ttu-id="13d5a-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="13d5a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="13d5a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="13d5a-121">Accept</span></span>|<span data-ttu-id="13d5a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="13d5a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="13d5a-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="13d5a-123">Request body</span></span>
<span data-ttu-id="13d5a-124">要求本文で、deviceComplianceDeviceStatus オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="13d5a-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="13d5a-125">次の表に、deviceComplianceDeviceStatus の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="13d5a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="13d5a-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="13d5a-126">Property</span></span>|<span data-ttu-id="13d5a-127">型</span><span class="sxs-lookup"><span data-stu-id="13d5a-127">Type</span></span>|<span data-ttu-id="13d5a-128">説明</span><span class="sxs-lookup"><span data-stu-id="13d5a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="13d5a-129">id</span><span class="sxs-lookup"><span data-stu-id="13d5a-129">id</span></span>|<span data-ttu-id="13d5a-130">String</span><span class="sxs-lookup"><span data-stu-id="13d5a-130">String</span></span>|<span data-ttu-id="13d5a-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="13d5a-131">Name of the entity.</span></span>|
|<span data-ttu-id="13d5a-132">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="13d5a-132">deviceDisplayName</span></span>|<span data-ttu-id="13d5a-133">String</span><span class="sxs-lookup"><span data-stu-id="13d5a-133">String</span></span>|<span data-ttu-id="13d5a-134">DevicePolicyStatus のデバイス名。</span><span class="sxs-lookup"><span data-stu-id="13d5a-134">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="13d5a-135">userName</span><span class="sxs-lookup"><span data-stu-id="13d5a-135">Username</span></span>|<span data-ttu-id="13d5a-136">String</span><span class="sxs-lookup"><span data-stu-id="13d5a-136">String</span></span>|<span data-ttu-id="13d5a-137">レポートされているユーザー名</span><span class="sxs-lookup"><span data-stu-id="13d5a-137">The User Name that is being reported</span></span>|
|<span data-ttu-id="13d5a-138">deviceModel</span><span class="sxs-lookup"><span data-stu-id="13d5a-138">deviceModel</span></span>|<span data-ttu-id="13d5a-139">String</span><span class="sxs-lookup"><span data-stu-id="13d5a-139">String</span></span>|<span data-ttu-id="13d5a-140">レポートされているデバイス モデル</span><span class="sxs-lookup"><span data-stu-id="13d5a-140">The device model that is being reported</span></span>|
|<span data-ttu-id="13d5a-141">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="13d5a-141">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="13d5a-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13d5a-142">DateTimeOffset</span></span>|<span data-ttu-id="13d5a-143">デバイス コンプライアンスの猶予期間が過ぎる DateTime</span><span class="sxs-lookup"><span data-stu-id="13d5a-143">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="13d5a-144">status</span><span class="sxs-lookup"><span data-stu-id="13d5a-144">status</span></span>|<span data-ttu-id="13d5a-145">String</span><span class="sxs-lookup"><span data-stu-id="13d5a-145">String</span></span>|<span data-ttu-id="13d5a-146">ポリシー レポートのコンプライアンスの状態。</span><span class="sxs-lookup"><span data-stu-id="13d5a-146">Compliance status of the policy report.</span></span> <span data-ttu-id="13d5a-147">可能な値は、`unknown`、`notApplicable`、`compliant`、`remediated`、`nonCompliant`、`error`、`conflict` です。</span><span class="sxs-lookup"><span data-stu-id="13d5a-147">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="13d5a-148">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="13d5a-148">lastReportedDateTime</span></span>|<span data-ttu-id="13d5a-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13d5a-149">DateTimeOffset</span></span>|<span data-ttu-id="13d5a-150">ポリシー レポートの最終変更日時。</span><span class="sxs-lookup"><span data-stu-id="13d5a-150">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="13d5a-151">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="13d5a-151">userPrincipalName</span></span>|<span data-ttu-id="13d5a-152">String</span><span class="sxs-lookup"><span data-stu-id="13d5a-152">String</span></span>|<span data-ttu-id="13d5a-153">UserPrincipalName。</span><span class="sxs-lookup"><span data-stu-id="13d5a-153">userPrincipalName</span></span>|



## <a name="response"></a><span data-ttu-id="13d5a-154">応答</span><span class="sxs-lookup"><span data-stu-id="13d5a-154">Response</span></span>
<span data-ttu-id="13d5a-155">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [deviceComplianceDeviceStatus](../resources/intune_deviceconfig_devicecompliancedevicestatus.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="13d5a-155">If successful, this method returns a `201 Created` response code and a [ListItemVersion](../resources/intune_deviceconfig_devicecompliancedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="13d5a-156">例</span><span class="sxs-lookup"><span data-stu-id="13d5a-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="13d5a-157">要求</span><span class="sxs-lookup"><span data-stu-id="13d5a-157">Request</span></span>
<span data-ttu-id="13d5a-158">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="13d5a-158">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatuses
Content-type: application/json
Content-length: 426

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceStatus",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="13d5a-159">応答</span><span class="sxs-lookup"><span data-stu-id="13d5a-159">Response</span></span>
<span data-ttu-id="13d5a-p103">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="13d5a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 475

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceStatus",
  "id": "c6c78124-8124-c6c7-2481-c7c62481c7c6",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```


