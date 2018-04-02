# <a name="create-mobileappcategory"></a><span data-ttu-id="09b5a-101">mobileAppCategory の作成</span><span class="sxs-lookup"><span data-stu-id="09b5a-101">Create mobileAppCategory</span></span>

> <span data-ttu-id="09b5a-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="09b5a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="09b5a-103">新しい [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="09b5a-103">Create a new [plannerBucket](../resources/intune_apps_mobileappcategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="09b5a-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="09b5a-104">Prerequisites</span></span>
<span data-ttu-id="09b5a-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09b5a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="09b5a-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="09b5a-107">Permission type</span></span>|<span data-ttu-id="09b5a-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="09b5a-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="09b5a-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="09b5a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="09b5a-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="09b5a-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="09b5a-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="09b5a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="09b5a-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="09b5a-112">Not supported.</span></span>|
|<span data-ttu-id="09b5a-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="09b5a-113">Application</span></span>|<span data-ttu-id="09b5a-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="09b5a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="09b5a-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="09b5a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppCategories
POST /deviceAppManagement/mobileApps/{mobileAppId}/categories
```

## <a name="request-headers"></a><span data-ttu-id="09b5a-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="09b5a-116">Request headers</span></span>
|<span data-ttu-id="09b5a-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="09b5a-117">Header</span></span>|<span data-ttu-id="09b5a-118">値</span><span class="sxs-lookup"><span data-stu-id="09b5a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="09b5a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="09b5a-119">Authorization</span></span>|<span data-ttu-id="09b5a-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="09b5a-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="09b5a-121">Accept</span><span class="sxs-lookup"><span data-stu-id="09b5a-121">Accept</span></span>|<span data-ttu-id="09b5a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="09b5a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="09b5a-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="09b5a-123">Request body</span></span>
<span data-ttu-id="09b5a-124">要求本文で、mobileAppCategory オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="09b5a-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="09b5a-125">次の表に、mobileAppCategory の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="09b5a-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="09b5a-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="09b5a-126">Property</span></span>|<span data-ttu-id="09b5a-127">型</span><span class="sxs-lookup"><span data-stu-id="09b5a-127">Type</span></span>|<span data-ttu-id="09b5a-128">説明</span><span class="sxs-lookup"><span data-stu-id="09b5a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="09b5a-129">id</span><span class="sxs-lookup"><span data-stu-id="09b5a-129">id</span></span>|<span data-ttu-id="09b5a-130">String</span><span class="sxs-lookup"><span data-stu-id="09b5a-130">String</span></span>|<span data-ttu-id="09b5a-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="09b5a-131">The key of the entity.</span></span>|
|<span data-ttu-id="09b5a-132">displayName</span><span class="sxs-lookup"><span data-stu-id="09b5a-132">displayName</span></span>|<span data-ttu-id="09b5a-133">String</span><span class="sxs-lookup"><span data-stu-id="09b5a-133">String</span></span>|<span data-ttu-id="09b5a-134">アプリのカテゴリの名前。</span><span class="sxs-lookup"><span data-stu-id="09b5a-134">The name of the category.</span></span>|
|<span data-ttu-id="09b5a-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="09b5a-135">lastModifiedDateTime</span></span>|<span data-ttu-id="09b5a-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="09b5a-136">DateTimeOffset</span></span>|<span data-ttu-id="09b5a-137">mobileAppCategory が最後に変更された日時。</span><span class="sxs-lookup"><span data-stu-id="09b5a-137">The date and time when the attachment was last modified.</span></span>|



## <a name="response"></a><span data-ttu-id="09b5a-138">応答</span><span class="sxs-lookup"><span data-stu-id="09b5a-138">Response</span></span>
<span data-ttu-id="09b5a-139">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [mobileAppCategory](../resources/intune_apps_mobileappcategory.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="09b5a-139">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_mobileappcategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="09b5a-140">例</span><span class="sxs-lookup"><span data-stu-id="09b5a-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="09b5a-141">要求</span><span class="sxs-lookup"><span data-stu-id="09b5a-141">Request</span></span>
<span data-ttu-id="09b5a-142">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="09b5a-142">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppCategories
Content-type: application/json
Content-length: 163

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```

### <a name="response"></a><span data-ttu-id="09b5a-143">応答</span><span class="sxs-lookup"><span data-stu-id="09b5a-143">Response</span></span>
<span data-ttu-id="09b5a-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="09b5a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 212

{
  "@odata.type": "#microsoft.graph.mobileAppCategory",
  "id": "d85d9cee-9cee-d85d-ee9c-5dd8ee9c5dd8",
  "displayName": "Display Name value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00"
}
```


