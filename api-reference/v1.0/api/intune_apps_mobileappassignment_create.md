# <a name="create-mobileappassignment"></a><span data-ttu-id="c7940-101">mobileAppAssignment の作成</span><span class="sxs-lookup"><span data-stu-id="c7940-101">Create mobileAppAssignment</span></span>

> <span data-ttu-id="c7940-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c7940-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7940-103">新しい [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c7940-103">Create a new [plannerBucket](../resources/intune_apps_mobileappassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7940-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="c7940-104">Prerequisites</span></span>
<span data-ttu-id="c7940-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c7940-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c7940-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="c7940-107">Permission type</span></span>|<span data-ttu-id="c7940-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="c7940-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7940-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="c7940-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c7940-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c7940-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="c7940-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="c7940-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7940-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c7940-112">Not supported.</span></span>|
|<span data-ttu-id="c7940-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c7940-113">Application</span></span>|<span data-ttu-id="c7940-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c7940-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7940-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="c7940-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="c7940-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c7940-116">Request headers</span></span>
|<span data-ttu-id="c7940-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c7940-117">Header</span></span>|<span data-ttu-id="c7940-118">値</span><span class="sxs-lookup"><span data-stu-id="c7940-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7940-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7940-119">Authorization</span></span>|<span data-ttu-id="c7940-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="c7940-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="c7940-121">Accept</span><span class="sxs-lookup"><span data-stu-id="c7940-121">Accept</span></span>|<span data-ttu-id="c7940-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c7940-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7940-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="c7940-123">Request body</span></span>
<span data-ttu-id="c7940-124">要求本文で、mobileAppAssignment オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="c7940-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="c7940-125">次の表に、mobileAppAssignment の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="c7940-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="c7940-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="c7940-126">Property</span></span>|<span data-ttu-id="c7940-127">型</span><span class="sxs-lookup"><span data-stu-id="c7940-127">Type</span></span>|<span data-ttu-id="c7940-128">説明</span><span class="sxs-lookup"><span data-stu-id="c7940-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c7940-129">id</span><span class="sxs-lookup"><span data-stu-id="c7940-129">id</span></span>|<span data-ttu-id="c7940-130">String</span><span class="sxs-lookup"><span data-stu-id="c7940-130">String</span></span>|<span data-ttu-id="c7940-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="c7940-131">Name of the entity.</span></span>|
|<span data-ttu-id="c7940-132">intent</span><span class="sxs-lookup"><span data-stu-id="c7940-132">Intent</span></span>|<span data-ttu-id="c7940-133">String</span><span class="sxs-lookup"><span data-stu-id="c7940-133">String</span></span>|<span data-ttu-id="c7940-134">管理者によって定義されたインストールの目的。可能な値は、`available`、`required`、`uninstall`、`availableWithoutEnrollment` です。</span><span class="sxs-lookup"><span data-stu-id="c7940-134">The install intent defined by the admin. Possible values are: `available`, `required`, `uninstall`, `availableWithoutEnrollment`.</span></span>|
|<span data-ttu-id="c7940-135">target</span><span class="sxs-lookup"><span data-stu-id="c7940-135">target</span></span>|[<span data-ttu-id="c7940-136">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="c7940-136">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_apps_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="c7940-137">管理者によって定義された、ターゲット グループの割り当て。</span><span class="sxs-lookup"><span data-stu-id="c7940-137">The target group assignment defined by the admin.</span></span>|
|<span data-ttu-id="c7940-138">settings</span><span class="sxs-lookup"><span data-stu-id="c7940-138">settings</span></span>|[<span data-ttu-id="c7940-139">mobileAppAssignmentSettings</span><span class="sxs-lookup"><span data-stu-id="c7940-139">mobileAppAssignmentSettings</span></span>](../resources/intune_apps_mobileappassignmentsettings.md)|<span data-ttu-id="c7940-140">管理者によって定義された、ターゲットの割り当ての設定。</span><span class="sxs-lookup"><span data-stu-id="c7940-140">The settings for target assignment defined by the admin.</span></span>|



## <a name="response"></a><span data-ttu-id="c7940-141">応答</span><span class="sxs-lookup"><span data-stu-id="c7940-141">Response</span></span>
<span data-ttu-id="c7940-142">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="c7940-142">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_mobileappassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7940-143">例</span><span class="sxs-lookup"><span data-stu-id="c7940-143">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7940-144">要求</span><span class="sxs-lookup"><span data-stu-id="c7940-144">Request</span></span>
<span data-ttu-id="c7940-145">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="c7940-145">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/assignments
Content-type: application/json
Content-length: 273

{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```

### <a name="response"></a><span data-ttu-id="c7940-146">応答</span><span class="sxs-lookup"><span data-stu-id="c7940-146">Response</span></span>
<span data-ttu-id="c7940-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="c7940-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 322

{
  "@odata.type": "#microsoft.graph.mobileAppAssignment",
  "id": "591620b7-20b7-5916-b720-1659b7201659",
  "intent": "required",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  },
  "settings": {
    "@odata.type": "microsoft.graph.mobileAppAssignmentSettings"
  }
}
```


