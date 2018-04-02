# <a name="list-managedebookassignments"></a><span data-ttu-id="6df2e-101">managedEBookAssignments のリスト</span><span class="sxs-lookup"><span data-stu-id="6df2e-101">List managedEBookAssignments</span></span>

> <span data-ttu-id="6df2e-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6df2e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6df2e-103">[managedEBookAssignment](../resources/intune_books_managedebookassignment.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="6df2e-103">List properties and relationships of the [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6df2e-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="6df2e-104">Prerequisites</span></span>
<span data-ttu-id="6df2e-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6df2e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6df2e-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="6df2e-107">Permission type</span></span>|<span data-ttu-id="6df2e-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="6df2e-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6df2e-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="6df2e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6df2e-110">DeviceManagementApps.ReadWrite.All、DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="6df2e-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="6df2e-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="6df2e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6df2e-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6df2e-112">Not supported.</span></span>|
|<span data-ttu-id="6df2e-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="6df2e-113">Application</span></span>|<span data-ttu-id="6df2e-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6df2e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6df2e-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="6df2e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="6df2e-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="6df2e-116">Request headers</span></span>
|<span data-ttu-id="6df2e-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="6df2e-117">Header</span></span>|<span data-ttu-id="6df2e-118">値</span><span class="sxs-lookup"><span data-stu-id="6df2e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6df2e-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6df2e-119">Authorization</span></span>|<span data-ttu-id="6df2e-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="6df2e-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="6df2e-121">Accept</span><span class="sxs-lookup"><span data-stu-id="6df2e-121">Accept</span></span>|<span data-ttu-id="6df2e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6df2e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6df2e-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="6df2e-123">Request body</span></span>
<span data-ttu-id="6df2e-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="6df2e-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6df2e-125">応答</span><span class="sxs-lookup"><span data-stu-id="6df2e-125">Response</span></span>
<span data-ttu-id="6df2e-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [managedEBookAssignment](../resources/intune_books_managedebookassignment.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="6df2e-126">If successful, this method returns a `200 OK` response code and collection of [workbookRangeView](../resources/intune_books_managedebookassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6df2e-127">例</span><span class="sxs-lookup"><span data-stu-id="6df2e-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="6df2e-128">要求</span><span class="sxs-lookup"><span data-stu-id="6df2e-128">Request</span></span>
<span data-ttu-id="6df2e-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="6df2e-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/assignments
```

### <a name="response"></a><span data-ttu-id="6df2e-130">応答</span><span class="sxs-lookup"><span data-stu-id="6df2e-130">Response</span></span>
<span data-ttu-id="6df2e-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="6df2e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 300

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedEBookAssignment",
      "id": "ae8b0d27-0d27-ae8b-270d-8bae270d8bae",
      "target": {
        "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
      },
      "installIntent": "required"
    }
  ]
}
```


