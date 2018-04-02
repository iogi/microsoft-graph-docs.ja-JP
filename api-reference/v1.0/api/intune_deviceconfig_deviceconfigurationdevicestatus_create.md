# <a name="create-deviceconfigurationdevicestatus"></a><span data-ttu-id="5f1f2-101">deviceConfigurationDeviceStatus の作成</span><span class="sxs-lookup"><span data-stu-id="5f1f2-101">Create deviceConfigurationDeviceStatus</span></span>

> <span data-ttu-id="5f1f2-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5f1f2-103">新しい [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-103">Create a new [plannerBucket](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5f1f2-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="5f1f2-104">Prerequisites</span></span>
<span data-ttu-id="5f1f2-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5f1f2-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="5f1f2-107">Permission type</span></span>|<span data-ttu-id="5f1f2-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="5f1f2-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5f1f2-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="5f1f2-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5f1f2-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5f1f2-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="5f1f2-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="5f1f2-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5f1f2-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-112">Not supported.</span></span>|
|<span data-ttu-id="5f1f2-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5f1f2-113">Application</span></span>|<span data-ttu-id="5f1f2-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5f1f2-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="5f1f2-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="5f1f2-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="5f1f2-116">Request headers</span></span>
|<span data-ttu-id="5f1f2-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="5f1f2-117">Header</span></span>|<span data-ttu-id="5f1f2-118">値</span><span class="sxs-lookup"><span data-stu-id="5f1f2-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5f1f2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5f1f2-119">Authorization</span></span>|<span data-ttu-id="5f1f2-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5f1f2-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5f1f2-121">Accept</span></span>|<span data-ttu-id="5f1f2-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5f1f2-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5f1f2-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="5f1f2-123">Request body</span></span>
<span data-ttu-id="5f1f2-124">要求本文で、deviceConfigurationDeviceStatus オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="5f1f2-125">次の表に、deviceConfigurationDeviceStatus の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="5f1f2-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5f1f2-126">Property</span></span>|<span data-ttu-id="5f1f2-127">型</span><span class="sxs-lookup"><span data-stu-id="5f1f2-127">Type</span></span>|<span data-ttu-id="5f1f2-128">説明</span><span class="sxs-lookup"><span data-stu-id="5f1f2-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5f1f2-129">id</span><span class="sxs-lookup"><span data-stu-id="5f1f2-129">id</span></span>|<span data-ttu-id="5f1f2-130">String</span><span class="sxs-lookup"><span data-stu-id="5f1f2-130">String</span></span>|<span data-ttu-id="5f1f2-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-131">Name of the entity.</span></span>|
|<span data-ttu-id="5f1f2-132">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="5f1f2-132">deviceDisplayName</span></span>|<span data-ttu-id="5f1f2-133">String</span><span class="sxs-lookup"><span data-stu-id="5f1f2-133">String</span></span>|<span data-ttu-id="5f1f2-134">DevicePolicyStatus のデバイス名。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-134">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="5f1f2-135">userName</span><span class="sxs-lookup"><span data-stu-id="5f1f2-135">Username</span></span>|<span data-ttu-id="5f1f2-136">String</span><span class="sxs-lookup"><span data-stu-id="5f1f2-136">String</span></span>|<span data-ttu-id="5f1f2-137">レポートされているユーザー名</span><span class="sxs-lookup"><span data-stu-id="5f1f2-137">The User Name that is being reported</span></span>|
|<span data-ttu-id="5f1f2-138">deviceModel</span><span class="sxs-lookup"><span data-stu-id="5f1f2-138">deviceModel</span></span>|<span data-ttu-id="5f1f2-139">String</span><span class="sxs-lookup"><span data-stu-id="5f1f2-139">String</span></span>|<span data-ttu-id="5f1f2-140">レポートされているデバイス モデル</span><span class="sxs-lookup"><span data-stu-id="5f1f2-140">The device model that is being reported</span></span>|
|<span data-ttu-id="5f1f2-141">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="5f1f2-141">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="5f1f2-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f1f2-142">DateTimeOffset</span></span>|<span data-ttu-id="5f1f2-143">デバイス コンプライアンスの猶予期間が過ぎる DateTime</span><span class="sxs-lookup"><span data-stu-id="5f1f2-143">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="5f1f2-144">status</span><span class="sxs-lookup"><span data-stu-id="5f1f2-144">status</span></span>|<span data-ttu-id="5f1f2-145">String</span><span class="sxs-lookup"><span data-stu-id="5f1f2-145">String</span></span>|<span data-ttu-id="5f1f2-146">ポリシー レポートのコンプライアンスの状態。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-146">Compliance status of the policy report.</span></span> <span data-ttu-id="5f1f2-147">可能な値は、`unknown`、`notApplicable`、`compliant`、`remediated`、`nonCompliant`、`error`、`conflict` です。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-147">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="5f1f2-148">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="5f1f2-148">lastReportedDateTime</span></span>|<span data-ttu-id="5f1f2-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5f1f2-149">DateTimeOffset</span></span>|<span data-ttu-id="5f1f2-150">ポリシー レポートの最終変更日時。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-150">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="5f1f2-151">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f1f2-151">userPrincipalName</span></span>|<span data-ttu-id="5f1f2-152">String</span><span class="sxs-lookup"><span data-stu-id="5f1f2-152">String</span></span>|<span data-ttu-id="5f1f2-153">UserPrincipalName。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-153">userPrincipalName</span></span>|



## <a name="response"></a><span data-ttu-id="5f1f2-154">応答</span><span class="sxs-lookup"><span data-stu-id="5f1f2-154">Response</span></span>
<span data-ttu-id="5f1f2-155">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-155">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5f1f2-156">例</span><span class="sxs-lookup"><span data-stu-id="5f1f2-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="5f1f2-157">要求</span><span class="sxs-lookup"><span data-stu-id="5f1f2-157">Request</span></span>
<span data-ttu-id="5f1f2-158">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-158">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
Content-type: application/json
Content-length: 429

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="5f1f2-159">応答</span><span class="sxs-lookup"><span data-stu-id="5f1f2-159">Response</span></span>
<span data-ttu-id="5f1f2-p103">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="5f1f2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 478

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
  "id": "674e98e5-98e5-674e-e598-4e67e5984e67",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```


