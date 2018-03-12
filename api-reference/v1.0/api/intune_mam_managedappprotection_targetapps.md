# <a name="targetapps-action"></a><span data-ttu-id="3b8ea-101">targetApps アクション</span><span class="sxs-lookup"><span data-stu-id="3b8ea-101">targetApps action</span></span>

> <span data-ttu-id="3b8ea-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3b8ea-103">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="3b8ea-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3b8ea-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="3b8ea-104">Prerequisites</span></span>
<span data-ttu-id="3b8ea-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3b8ea-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="3b8ea-107">Permission type</span></span>|<span data-ttu-id="3b8ea-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="3b8ea-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3b8ea-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="3b8ea-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3b8ea-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3b8ea-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="3b8ea-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="3b8ea-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3b8ea-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-112">Not supported.</span></span>|
|<span data-ttu-id="3b8ea-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3b8ea-113">Application</span></span>|<span data-ttu-id="3b8ea-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3b8ea-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="3b8ea-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/targetApps
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/appliedPolicies/{managedAppPolicyId}/targetApps
POST /deviceAppManagement/managedAppRegistrations/{managedAppRegistrationId}/intendedPolicies/{managedAppPolicyId}/targetApps
```

## <a name="request-headers"></a><span data-ttu-id="3b8ea-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="3b8ea-116">Request headers</span></span>
|<span data-ttu-id="3b8ea-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="3b8ea-117">Header</span></span>|<span data-ttu-id="3b8ea-118">値</span><span class="sxs-lookup"><span data-stu-id="3b8ea-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3b8ea-119">承認</span><span class="sxs-lookup"><span data-stu-id="3b8ea-119">Authorization</span></span>|<span data-ttu-id="3b8ea-120">ベアラー &lt;トークン&gt;が必須。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="3b8ea-121">承諾</span><span class="sxs-lookup"><span data-stu-id="3b8ea-121">Accept</span></span>|<span data-ttu-id="3b8ea-122">application/json</span><span class="sxs-lookup"><span data-stu-id="3b8ea-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3b8ea-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="3b8ea-123">Request body</span></span>
<span data-ttu-id="3b8ea-124">要求本文で、パラメーターの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-124">In the request body, supply a JSON representation of the Contact object.</span></span>

<span data-ttu-id="3b8ea-125">次の表は、このアクションで使用できるパラメーターを示しています。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="3b8ea-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="3b8ea-126">Property</span></span>|<span data-ttu-id="3b8ea-127">型</span><span class="sxs-lookup"><span data-stu-id="3b8ea-127">Type</span></span>|<span data-ttu-id="3b8ea-128">説明</span><span class="sxs-lookup"><span data-stu-id="3b8ea-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3b8ea-129">apps</span><span class="sxs-lookup"><span data-stu-id="3b8ea-129">apps</span></span>|<span data-ttu-id="3b8ea-130">[managedMobileApp](../resources/intune_mam_managedmobileapp.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="3b8ea-130">[managedMobileApp](../resources/intune_mam_managedmobileapp.md) collection</span></span>|<span data-ttu-id="3b8ea-131">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="3b8ea-131">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="3b8ea-132">応答</span><span class="sxs-lookup"><span data-stu-id="3b8ea-132">Response</span></span>
<span data-ttu-id="3b8ea-133">成功した場合、このアクションは `204 No Content` 応答コードを返します。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-133">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="3b8ea-134">例</span><span class="sxs-lookup"><span data-stu-id="3b8ea-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="3b8ea-135">要求</span><span class="sxs-lookup"><span data-stu-id="3b8ea-135">Request</span></span>
<span data-ttu-id="3b8ea-136">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedAppPolicies/{managedAppPolicyId}/targetApps

Content-type: application/json
Content-length: 286

{
  "apps": [
    {
      "@odata.type": "#microsoft.graph.managedMobileApp",
      "mobileAppIdentifier": {
        "@odata.type": "microsoft.graph.mobileAppIdentifier"
      },
      "id": "0a129715-9715-0a12-1597-120a1597120a",
      "version": "Version value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="3b8ea-137">応答</span><span class="sxs-lookup"><span data-stu-id="3b8ea-137">Response</span></span>
<span data-ttu-id="3b8ea-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="3b8ea-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```


