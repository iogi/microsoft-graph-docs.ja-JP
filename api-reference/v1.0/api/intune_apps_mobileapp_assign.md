# <a name="assign-action"></a><span data-ttu-id="b6883-101">assign アクション</span><span class="sxs-lookup"><span data-stu-id="b6883-101">assign action</span></span>

> <span data-ttu-id="b6883-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b6883-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6883-103">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="b6883-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6883-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="b6883-104">Prerequisites</span></span>
<span data-ttu-id="b6883-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b6883-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b6883-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="b6883-107">Permission type</span></span>|<span data-ttu-id="b6883-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="b6883-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b6883-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="b6883-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b6883-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6883-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="b6883-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="b6883-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b6883-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b6883-112">Not supported.</span></span>|
|<span data-ttu-id="b6883-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b6883-113">Application</span></span>|<span data-ttu-id="b6883-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b6883-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b6883-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="b6883-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/assign
```

## <a name="request-headers"></a><span data-ttu-id="b6883-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b6883-116">Request headers</span></span>
|<span data-ttu-id="b6883-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b6883-117">Header</span></span>|<span data-ttu-id="b6883-118">値</span><span class="sxs-lookup"><span data-stu-id="b6883-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b6883-119">承認</span><span class="sxs-lookup"><span data-stu-id="b6883-119">Authorization</span></span>|<span data-ttu-id="b6883-120">ベアラー &lt;トークン&gt;が必須。</span><span class="sxs-lookup"><span data-stu-id="b6883-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="b6883-121">承諾</span><span class="sxs-lookup"><span data-stu-id="b6883-121">Accept</span></span>|<span data-ttu-id="b6883-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b6883-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6883-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="b6883-123">Request body</span></span>
<span data-ttu-id="b6883-124">要求本文で、パラメーターの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="b6883-124">In the request body, supply a JSON representation of the Contact object.</span></span>

<span data-ttu-id="b6883-125">次の表は、このアクションで使用できるパラメーターを示しています。</span><span class="sxs-lookup"><span data-stu-id="b6883-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="b6883-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b6883-126">Property</span></span>|<span data-ttu-id="b6883-127">型</span><span class="sxs-lookup"><span data-stu-id="b6883-127">Type</span></span>|<span data-ttu-id="b6883-128">説明</span><span class="sxs-lookup"><span data-stu-id="b6883-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b6883-129">mobileAppAssignments</span><span class="sxs-lookup"><span data-stu-id="b6883-129">mobileAppAssignments</span></span>|<span data-ttu-id="b6883-130">[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="b6883-130">[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) collection</span></span>|<span data-ttu-id="b6883-131">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="b6883-131">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="b6883-132">応答</span><span class="sxs-lookup"><span data-stu-id="b6883-132">Response</span></span>
<span data-ttu-id="b6883-133">成功した場合、このアクションは `204 No Content` 応答コードを返します。</span><span class="sxs-lookup"><span data-stu-id="b6883-133">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="b6883-134">例</span><span class="sxs-lookup"><span data-stu-id="b6883-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="b6883-135">要求</span><span class="sxs-lookup"><span data-stu-id="b6883-135">Request</span></span>
<span data-ttu-id="b6883-136">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="b6883-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}/assign

Content-type: application/json
Content-length: 406

{
  "mobileAppAssignments": [
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
  ]
}
```

### <a name="response"></a><span data-ttu-id="b6883-137">応答</span><span class="sxs-lookup"><span data-stu-id="b6883-137">Response</span></span>
<span data-ttu-id="b6883-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="b6883-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```


