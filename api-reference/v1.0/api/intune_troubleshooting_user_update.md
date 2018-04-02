# <a name="update-user"></a><span data-ttu-id="27c79-101">user の更新</span><span class="sxs-lookup"><span data-stu-id="27c79-101">Update user</span></span>

> <span data-ttu-id="27c79-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="27c79-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="27c79-103">[user](../resources/intune_troubleshooting_user.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="27c79-103">Update the properties of a user object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="27c79-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="27c79-104">Prerequisites</span></span>
<span data-ttu-id="27c79-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="27c79-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="27c79-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="27c79-107">Permission type</span></span>|<span data-ttu-id="27c79-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="27c79-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="27c79-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="27c79-109">Delegated (work or school account)</span></span>|<span data-ttu-id="27c79-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="27c79-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="27c79-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="27c79-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="27c79-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="27c79-112">Not supported.</span></span>|
|<span data-ttu-id="27c79-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="27c79-113">Application</span></span>|<span data-ttu-id="27c79-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="27c79-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="27c79-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="27c79-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}
```

## <a name="request-headers"></a><span data-ttu-id="27c79-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="27c79-116">Request headers</span></span>
|<span data-ttu-id="27c79-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="27c79-117">Header</span></span>|<span data-ttu-id="27c79-118">値</span><span class="sxs-lookup"><span data-stu-id="27c79-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="27c79-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="27c79-119">Authorization</span></span>|<span data-ttu-id="27c79-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="27c79-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="27c79-121">Accept</span><span class="sxs-lookup"><span data-stu-id="27c79-121">Accept</span></span>|<span data-ttu-id="27c79-122">application/json</span><span class="sxs-lookup"><span data-stu-id="27c79-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="27c79-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="27c79-123">Request body</span></span>
<span data-ttu-id="27c79-124">要求本文で、[user](../resources/intune_troubleshooting_user.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="27c79-124">In the request body, supply a JSON representation of [user](../resources/intune_troubleshooting_user.md) object.</span></span>

<span data-ttu-id="27c79-125">次の表に、[user](../resources/intune_troubleshooting_user.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="27c79-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="27c79-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="27c79-126">Property</span></span>|<span data-ttu-id="27c79-127">型</span><span class="sxs-lookup"><span data-stu-id="27c79-127">Type</span></span>|<span data-ttu-id="27c79-128">説明</span><span class="sxs-lookup"><span data-stu-id="27c79-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="27c79-129">id</span><span class="sxs-lookup"><span data-stu-id="27c79-129">id</span></span>|<span data-ttu-id="27c79-130">String</span><span class="sxs-lookup"><span data-stu-id="27c79-130">String</span></span>|<span data-ttu-id="27c79-131">ユーザーの一意識別子</span><span class="sxs-lookup"><span data-stu-id="27c79-131">Unique identifier for the lab user.</span></span>|



## <a name="response"></a><span data-ttu-id="27c79-132">応答</span><span class="sxs-lookup"><span data-stu-id="27c79-132">Response</span></span>
<span data-ttu-id="27c79-133">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [user](../resources/intune_troubleshooting_user.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="27c79-133">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_troubleshooting_user.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="27c79-134">例</span><span class="sxs-lookup"><span data-stu-id="27c79-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="27c79-135">要求</span><span class="sxs-lookup"><span data-stu-id="27c79-135">Request</span></span>
<span data-ttu-id="27c79-136">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="27c79-136">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="27c79-137">応答</span><span class="sxs-lookup"><span data-stu-id="27c79-137">Response</span></span>
<span data-ttu-id="27c79-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="27c79-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 95

{
  "@odata.type": "#microsoft.graph.user",
  "id": "d36894ae-94ae-d368-ae94-68d3ae9468d3"
}
```


