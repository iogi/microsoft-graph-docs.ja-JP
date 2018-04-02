# <a name="update-managedappstatusraw"></a><span data-ttu-id="b0f8e-101">managedAppStatusRaw の更新</span><span class="sxs-lookup"><span data-stu-id="b0f8e-101">Update managedAppStatusRaw</span></span>

> <span data-ttu-id="b0f8e-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b0f8e-103">[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-103">Update the properties of a [calendar](../resources/intune_mam_managedappstatusraw.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b0f8e-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="b0f8e-104">Prerequisites</span></span>
<span data-ttu-id="b0f8e-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b0f8e-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="b0f8e-107">Permission type</span></span>|<span data-ttu-id="b0f8e-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="b0f8e-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b0f8e-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="b0f8e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b0f8e-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b0f8e-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b0f8e-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="b0f8e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b0f8e-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-112">Not supported.</span></span>|
|<span data-ttu-id="b0f8e-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b0f8e-113">Application</span></span>|<span data-ttu-id="b0f8e-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b0f8e-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="b0f8e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedAppStatuses/{managedAppStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="b0f8e-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b0f8e-116">Request headers</span></span>
|<span data-ttu-id="b0f8e-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b0f8e-117">Header</span></span>|<span data-ttu-id="b0f8e-118">値</span><span class="sxs-lookup"><span data-stu-id="b0f8e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b0f8e-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="b0f8e-119">Authorization</span></span>|<span data-ttu-id="b0f8e-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="b0f8e-121">Accept</span><span class="sxs-lookup"><span data-stu-id="b0f8e-121">Accept</span></span>|<span data-ttu-id="b0f8e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b0f8e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b0f8e-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="b0f8e-123">Request body</span></span>
<span data-ttu-id="b0f8e-124">要求本文で、[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_mam_managedappstatusraw.md) object.</span></span>

<span data-ttu-id="b0f8e-125">次の表に、[managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="b0f8e-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b0f8e-126">Property</span></span>|<span data-ttu-id="b0f8e-127">型</span><span class="sxs-lookup"><span data-stu-id="b0f8e-127">Type</span></span>|<span data-ttu-id="b0f8e-128">説明</span><span class="sxs-lookup"><span data-stu-id="b0f8e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b0f8e-129">displayName</span><span class="sxs-lookup"><span data-stu-id="b0f8e-129">displayName</span></span>|<span data-ttu-id="b0f8e-130">String</span><span class="sxs-lookup"><span data-stu-id="b0f8e-130">String</span></span>|<span data-ttu-id="b0f8e-131">進捗レポートのフレンドリ名。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-131">Friendly name of the status report.</span></span> <span data-ttu-id="b0f8e-132">[managedAppStatus](../resources/intune_mam_managedappstatus.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b0f8e-132">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="b0f8e-133">id</span><span class="sxs-lookup"><span data-stu-id="b0f8e-133">id</span></span>|<span data-ttu-id="b0f8e-134">String</span><span class="sxs-lookup"><span data-stu-id="b0f8e-134">String</span></span>|<span data-ttu-id="b0f8e-135">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-135">Name of the entity.</span></span> <span data-ttu-id="b0f8e-136">[managedAppStatus](../resources/intune_mam_managedappstatus.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b0f8e-136">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="b0f8e-137">version</span><span class="sxs-lookup"><span data-stu-id="b0f8e-137">version</span></span>|<span data-ttu-id="b0f8e-138">String</span><span class="sxs-lookup"><span data-stu-id="b0f8e-138">String</span></span>|<span data-ttu-id="b0f8e-139">エンティティのバージョン。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-139">Version of the entity.</span></span> <span data-ttu-id="b0f8e-140">[managedAppStatus](../resources/intune_mam_managedappstatus.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b0f8e-140">Inherited from [managedAppStatus](../resources/intune_mam_managedappstatus.md)</span></span>|
|<span data-ttu-id="b0f8e-141">content</span><span class="sxs-lookup"><span data-stu-id="b0f8e-141">content</span></span>|[<span data-ttu-id="b0f8e-142">Json</span><span class="sxs-lookup"><span data-stu-id="b0f8e-142">json</span></span>](../resources/intune_mam_json.md)|<span data-ttu-id="b0f8e-143">進捗レポートの内容。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-143">Status report content.</span></span>|



## <a name="response"></a><span data-ttu-id="b0f8e-144">応答</span><span class="sxs-lookup"><span data-stu-id="b0f8e-144">Response</span></span>
<span data-ttu-id="b0f8e-145">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [managedAppStatusRaw](../resources/intune_mam_managedappstatusraw.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-145">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_mam_managedappstatusraw.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b0f8e-146">例</span><span class="sxs-lookup"><span data-stu-id="b0f8e-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="b0f8e-147">要求</span><span class="sxs-lookup"><span data-stu-id="b0f8e-147">Request</span></span>
<span data-ttu-id="b0f8e-148">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-148">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppStatuses/{managedAppStatusId}
Content-type: application/json
Content-length: 139

{
  "displayName": "Display Name value",
  "version": "Version value",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```

### <a name="response"></a><span data-ttu-id="b0f8e-149">応答</span><span class="sxs-lookup"><span data-stu-id="b0f8e-149">Response</span></span>
<span data-ttu-id="b0f8e-p105">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="b0f8e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 246

{
  "@odata.type": "#microsoft.graph.managedAppStatusRaw",
  "displayName": "Display Name value",
  "id": "80847581-7581-8084-8175-848081758480",
  "version": "Version value",
  "content": {
    "@odata.type": "microsoft.graph.Json"
  }
}
```


