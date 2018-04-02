# <a name="create-auditevent"></a><span data-ttu-id="bb51a-101">auditEvent の作成</span><span class="sxs-lookup"><span data-stu-id="bb51a-101">Create auditEvent</span></span>

> <span data-ttu-id="bb51a-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb51a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bb51a-103">新しい [auditEvent](../resources/intune_auditing_auditevent.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="bb51a-103">Create a new [plannerBucket](../resources/intune_auditing_auditevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bb51a-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="bb51a-104">Prerequisites</span></span>
<span data-ttu-id="bb51a-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bb51a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bb51a-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="bb51a-107">Permission type</span></span>|<span data-ttu-id="bb51a-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="bb51a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bb51a-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="bb51a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bb51a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bb51a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bb51a-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="bb51a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bb51a-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bb51a-112">Not supported.</span></span>|
|<span data-ttu-id="bb51a-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="bb51a-113">Application</span></span>|<span data-ttu-id="bb51a-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="bb51a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bb51a-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="bb51a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/auditEvents
```

## <a name="request-headers"></a><span data-ttu-id="bb51a-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="bb51a-116">Request headers</span></span>
|<span data-ttu-id="bb51a-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="bb51a-117">Header</span></span>|<span data-ttu-id="bb51a-118">値</span><span class="sxs-lookup"><span data-stu-id="bb51a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bb51a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="bb51a-119">Authorization</span></span>|<span data-ttu-id="bb51a-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="bb51a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="bb51a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="bb51a-121">Accept</span></span>|<span data-ttu-id="bb51a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="bb51a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bb51a-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="bb51a-123">Request body</span></span>
<span data-ttu-id="bb51a-124">要求本文で、auditEvent オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="bb51a-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="bb51a-125">次の表に、auditEvent の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="bb51a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="bb51a-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="bb51a-126">Property</span></span>|<span data-ttu-id="bb51a-127">型</span><span class="sxs-lookup"><span data-stu-id="bb51a-127">Type</span></span>|<span data-ttu-id="bb51a-128">説明</span><span class="sxs-lookup"><span data-stu-id="bb51a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bb51a-129">id</span><span class="sxs-lookup"><span data-stu-id="bb51a-129">id</span></span>|<span data-ttu-id="bb51a-130">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-130">String</span></span>|<span data-ttu-id="bb51a-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="bb51a-131">Name of the entity.</span></span>|
|<span data-ttu-id="bb51a-132">displayName</span><span class="sxs-lookup"><span data-stu-id="bb51a-132">displayName</span></span>|<span data-ttu-id="bb51a-133">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-133">String</span></span>|<span data-ttu-id="bb51a-134">イベントの表示名。</span><span class="sxs-lookup"><span data-stu-id="bb51a-134">Event display name.</span></span>|
|<span data-ttu-id="bb51a-135">componentName</span><span class="sxs-lookup"><span data-stu-id="bb51a-135">--componentName</span></span>|<span data-ttu-id="bb51a-136">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-136">String</span></span>|<span data-ttu-id="bb51a-137">コンポーネント名。</span><span class="sxs-lookup"><span data-stu-id="bb51a-137">Component name.</span></span>|
|<span data-ttu-id="bb51a-138">actor</span><span class="sxs-lookup"><span data-stu-id="bb51a-138">actor</span></span>|[<span data-ttu-id="bb51a-139">auditActor</span><span class="sxs-lookup"><span data-stu-id="bb51a-139">auditActor</span></span>](../resources/intune_auditing_auditactor.md)|<span data-ttu-id="bb51a-140">監査イベントに関連付けられている AAD ユーザーとアプリケーション。</span><span class="sxs-lookup"><span data-stu-id="bb51a-140">AAD user and application that are associated with the audit event.</span></span>|
|<span data-ttu-id="bb51a-141">アクティビティ</span><span class="sxs-lookup"><span data-stu-id="bb51a-141">activity</span></span>|<span data-ttu-id="bb51a-142">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-142">String</span></span>|<span data-ttu-id="bb51a-143">アクティビティのフレンドリ名。</span><span class="sxs-lookup"><span data-stu-id="bb51a-143">Friendly name of the activity.</span></span>|
|<span data-ttu-id="bb51a-144">activityDateTime</span><span class="sxs-lookup"><span data-stu-id="bb51a-144">activityDateTime</span></span>|<span data-ttu-id="bb51a-145">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb51a-145">DateTimeOffset</span></span>|<span data-ttu-id="bb51a-146">アクティビティが実行された日時 (UTC)。</span><span class="sxs-lookup"><span data-stu-id="bb51a-146">The date time in UTC when the activity was performed.</span></span>|
|<span data-ttu-id="bb51a-147">activityType</span><span class="sxs-lookup"><span data-stu-id="bb51a-147">activityType</span></span>|<span data-ttu-id="bb51a-148">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-148">String</span></span>|<span data-ttu-id="bb51a-149">実行されたアクティビティの種類。</span><span class="sxs-lookup"><span data-stu-id="bb51a-149">The type of activity that was being performed.</span></span>|
|<span data-ttu-id="bb51a-150">activityOperationType</span><span class="sxs-lookup"><span data-stu-id="bb51a-150">activityOperationType</span></span>|<span data-ttu-id="bb51a-151">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-151">String</span></span>|<span data-ttu-id="bb51a-152">アクティビティの HTTP 操作の種類。</span><span class="sxs-lookup"><span data-stu-id="bb51a-152">The HTTP operation type of the activity.</span></span>|
|<span data-ttu-id="bb51a-153">activityResult</span><span class="sxs-lookup"><span data-stu-id="bb51a-153">activityResult</span></span>|<span data-ttu-id="bb51a-154">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-154">String</span></span>|<span data-ttu-id="bb51a-155">アクティビティの結果。</span><span class="sxs-lookup"><span data-stu-id="bb51a-155">The result of the submission.</span></span>|
|<span data-ttu-id="bb51a-156">correlationId</span><span class="sxs-lookup"><span data-stu-id="bb51a-156">correlation_id</span></span>|<span data-ttu-id="bb51a-157">Guid</span><span class="sxs-lookup"><span data-stu-id="bb51a-157">Guid</span></span>|<span data-ttu-id="bb51a-158">システム内でのアクティビティの相互関連付けに使用されるクライアント要求 ID。</span><span class="sxs-lookup"><span data-stu-id="bb51a-158">The client request Id that is used to correlate activity within the system.</span></span>|
|<span data-ttu-id="bb51a-159">resources</span><span class="sxs-lookup"><span data-stu-id="bb51a-159">resources</span></span>|<span data-ttu-id="bb51a-160">[auditResource](../resources/intune_auditing_auditresource.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="bb51a-160">[auditResource](../resources/intune_auditing_auditresource.md) collection</span></span>|<span data-ttu-id="bb51a-161">変更中のリソースです。</span><span class="sxs-lookup"><span data-stu-id="bb51a-161">Resources being modified.</span></span>|
|<span data-ttu-id="bb51a-162">category</span><span class="sxs-lookup"><span data-stu-id="bb51a-162">category</span></span>|<span data-ttu-id="bb51a-163">String</span><span class="sxs-lookup"><span data-stu-id="bb51a-163">String</span></span>|<span data-ttu-id="bb51a-164">監査のカテゴリです。</span><span class="sxs-lookup"><span data-stu-id="bb51a-164">Audit category.</span></span>|



## <a name="response"></a><span data-ttu-id="bb51a-165">応答</span><span class="sxs-lookup"><span data-stu-id="bb51a-165">Response</span></span>
<span data-ttu-id="bb51a-166">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [auditEvent](../resources/intune_auditing_auditevent.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="bb51a-166">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_auditing_auditevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bb51a-167">例</span><span class="sxs-lookup"><span data-stu-id="bb51a-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="bb51a-168">要求</span><span class="sxs-lookup"><span data-stu-id="bb51a-168">Request</span></span>
<span data-ttu-id="bb51a-169">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="bb51a-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/auditEvents
Content-type: application/json
Content-length: 1444

{
  "@odata.type": "#microsoft.graph.auditEvent",
  "displayName": "Display Name value",
  "componentName": "Component Name value",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "Type value",
    "permissions": [
      "Permissions value"
    ],
    "userPermissions": [
      "User Permissions value"
    ],
    "applicationId": "Application Id value",
    "applicationDisplayName": "Application Display Name value",
    "userPrincipalName": "User Principal Name value",
    "servicePrincipalName": "Service Principal Name value",
    "ipAddress": "Ip Address value",
    "userId": "User Id value"
  },
  "activity": "Activity value",
  "activityDateTime": "2016-12-31T23:59:51.6363086-08:00",
  "activityType": "Activity Type value",
  "activityOperationType": "Activity Operation Type value",
  "activityResult": "Activity Result value",
  "correlationId": "<Unknown Primitive Type Edm.Guid>",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "Display Name value",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "Display Name value",
          "oldValue": "Old Value value",
          "newValue": "New Value value"
        }
      ],
      "type": "Type value",
      "resourceId": "Resource Id value"
    }
  ],
  "category": "Category value"
}
```

### <a name="response"></a><span data-ttu-id="bb51a-170">応答</span><span class="sxs-lookup"><span data-stu-id="bb51a-170">Response</span></span>
<span data-ttu-id="bb51a-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="bb51a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1493

{
  "@odata.type": "#microsoft.graph.auditEvent",
  "id": "59653ce8-3ce8-5965-e83c-6559e83c6559",
  "displayName": "Display Name value",
  "componentName": "Component Name value",
  "actor": {
    "@odata.type": "microsoft.graph.auditActor",
    "type": "Type value",
    "permissions": [
      "Permissions value"
    ],
    "userPermissions": [
      "User Permissions value"
    ],
    "applicationId": "Application Id value",
    "applicationDisplayName": "Application Display Name value",
    "userPrincipalName": "User Principal Name value",
    "servicePrincipalName": "Service Principal Name value",
    "ipAddress": "Ip Address value",
    "userId": "User Id value"
  },
  "activity": "Activity value",
  "activityDateTime": "2016-12-31T23:59:51.6363086-08:00",
  "activityType": "Activity Type value",
  "activityOperationType": "Activity Operation Type value",
  "activityResult": "Activity Result value",
  "correlationId": "<Unknown Primitive Type Edm.Guid>",
  "resources": [
    {
      "@odata.type": "microsoft.graph.auditResource",
      "displayName": "Display Name value",
      "modifiedProperties": [
        {
          "@odata.type": "microsoft.graph.auditProperty",
          "displayName": "Display Name value",
          "oldValue": "Old Value value",
          "newValue": "New Value value"
        }
      ],
      "type": "Type value",
      "resourceId": "Resource Id value"
    }
  ],
  "category": "Category value"
}
```


