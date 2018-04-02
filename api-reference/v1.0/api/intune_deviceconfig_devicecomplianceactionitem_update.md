# <a name="update-devicecomplianceactionitem"></a><span data-ttu-id="8a7b3-101">deviceComplianceActionItem の更新</span><span class="sxs-lookup"><span data-stu-id="8a7b3-101">Update deviceComplianceActionItem</span></span>

> <span data-ttu-id="8a7b3-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8a7b3-103">[deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-103">Update the properties of a [calendar](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8a7b3-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="8a7b3-104">Prerequisites</span></span>
<span data-ttu-id="8a7b3-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8a7b3-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="8a7b3-107">Permission type</span></span>|<span data-ttu-id="8a7b3-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="8a7b3-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8a7b3-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="8a7b3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8a7b3-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a7b3-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8a7b3-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="8a7b3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8a7b3-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-112">Not supported.</span></span>|
|<span data-ttu-id="8a7b3-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="8a7b3-113">Application</span></span>|<span data-ttu-id="8a7b3-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8a7b3-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="8a7b3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
```

## <a name="request-headers"></a><span data-ttu-id="8a7b3-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="8a7b3-116">Request headers</span></span>
|<span data-ttu-id="8a7b3-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="8a7b3-117">Header</span></span>|<span data-ttu-id="8a7b3-118">値</span><span class="sxs-lookup"><span data-stu-id="8a7b3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8a7b3-119">承認</span><span class="sxs-lookup"><span data-stu-id="8a7b3-119">Authorization</span></span>|<span data-ttu-id="8a7b3-120">ベアラー &lt;トークン&gt;が必須。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="8a7b3-121">承諾</span><span class="sxs-lookup"><span data-stu-id="8a7b3-121">Accept</span></span>|<span data-ttu-id="8a7b3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8a7b3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8a7b3-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="8a7b3-123">Request body</span></span>
<span data-ttu-id="8a7b3-124">要求本文で、[deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object.</span></span>

<span data-ttu-id="8a7b3-125">次の表に、[deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="8a7b3-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8a7b3-126">Property</span></span>|<span data-ttu-id="8a7b3-127">型</span><span class="sxs-lookup"><span data-stu-id="8a7b3-127">Type</span></span>|<span data-ttu-id="8a7b3-128">説明</span><span class="sxs-lookup"><span data-stu-id="8a7b3-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8a7b3-129">id</span><span class="sxs-lookup"><span data-stu-id="8a7b3-129">id</span></span>|<span data-ttu-id="8a7b3-130">String</span><span class="sxs-lookup"><span data-stu-id="8a7b3-130">String</span></span>|<span data-ttu-id="8a7b3-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-131">Name of the entity.</span></span>|
|<span data-ttu-id="8a7b3-132">gracePeriodHours</span><span class="sxs-lookup"><span data-stu-id="8a7b3-132">gracePeriodHours</span></span>|<span data-ttu-id="8a7b3-133">Int32</span><span class="sxs-lookup"><span data-stu-id="8a7b3-133">Int32</span></span>|<span data-ttu-id="8a7b3-134">アクションが実行されるまでの待機時間。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-134">Number of hours to wait till the action will be enforced.</span></span> <span data-ttu-id="8a7b3-135">有効な値は 0 から 8760 までです</span><span class="sxs-lookup"><span data-stu-id="8a7b3-135">Valid values 0 to 8760</span></span>|
|<span data-ttu-id="8a7b3-136">actionType</span><span class="sxs-lookup"><span data-stu-id="8a7b3-136">actionType</span></span>|<span data-ttu-id="8a7b3-137">String</span><span class="sxs-lookup"><span data-stu-id="8a7b3-137">String</span></span>|<span data-ttu-id="8a7b3-138">実施するアクション。可能な値は、`noAction`、`notification`、`block`、`retire`、`wipe`、`removeResourceAccessProfiles` です。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-138">What action to take Possible values are: `noAction`, `notification`, `block`, `retire`, `wipe`, `removeResourceAccessProfiles`.</span></span>|
|<span data-ttu-id="8a7b3-139">notificationTemplateId</span><span class="sxs-lookup"><span data-stu-id="8a7b3-139">notificationTemplateId</span></span>|<span data-ttu-id="8a7b3-140">String</span><span class="sxs-lookup"><span data-stu-id="8a7b3-140">String</span></span>|<span data-ttu-id="8a7b3-141">使用する通知メッセージ テンプレート</span><span class="sxs-lookup"><span data-stu-id="8a7b3-141">What notification Message template to use</span></span>|
|<span data-ttu-id="8a7b3-142">notificationMessageCCList</span><span class="sxs-lookup"><span data-stu-id="8a7b3-142">notificationMessageCCList</span></span>|<span data-ttu-id="8a7b3-143">String コレクション</span><span class="sxs-lookup"><span data-stu-id="8a7b3-143">String collection</span></span>|<span data-ttu-id="8a7b3-144">この通知メッセージの CC に設定するグループ ID のリスト。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-144">A list of group IDs to speicify who to CC this notification message to.</span></span>|



## <a name="response"></a><span data-ttu-id="8a7b3-145">応答</span><span class="sxs-lookup"><span data-stu-id="8a7b3-145">Response</span></span>
<span data-ttu-id="8a7b3-146">成功した場合、このメソッドは `200 OK` 応答コードと、更新された [deviceComplianceActionItem](../resources/intune_deviceconfig_devicecomplianceactionitem.md) オブジェクトを応答本文で返します。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-146">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_devicecomplianceactionitem.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8a7b3-147">例</span><span class="sxs-lookup"><span data-stu-id="8a7b3-147">Example</span></span>
### <a name="request"></a><span data-ttu-id="8a7b3-148">要求</span><span class="sxs-lookup"><span data-stu-id="8a7b3-148">Request</span></span>
<span data-ttu-id="8a7b3-149">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-149">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}/scheduledActionConfigurations/{deviceComplianceActionItemId}
Content-type: application/json
Content-length: 206

{
  "gracePeriodHours": 0,
  "actionType": "notification",
  "notificationTemplateId": "Notification Template Id value",
  "notificationMessageCCList": [
    "Notification Message CCList value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="8a7b3-150">応答</span><span class="sxs-lookup"><span data-stu-id="8a7b3-150">Response</span></span>
<span data-ttu-id="8a7b3-p103">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="8a7b3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 320

{
  "@odata.type": "#microsoft.graph.deviceComplianceActionItem",
  "id": "e01a1893-1893-e01a-9318-1ae093181ae0",
  "gracePeriodHours": 0,
  "actionType": "notification",
  "notificationTemplateId": "Notification Template Id value",
  "notificationMessageCCList": [
    "Notification Message CCList value"
  ]
}
```


