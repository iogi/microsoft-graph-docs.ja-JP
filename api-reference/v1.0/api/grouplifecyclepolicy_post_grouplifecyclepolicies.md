# <a name="create-grouplifecyclepolicy"></a><span data-ttu-id="23cd1-101">Create groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="23cd1-101">Create groupLifecyclePolicy</span></span>

<span data-ttu-id="23cd1-102">新しい [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) を作成します。</span><span class="sxs-lookup"><span data-stu-id="23cd1-102">Creates a new [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="23cd1-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="23cd1-103">Permissions</span></span>

<span data-ttu-id="23cd1-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="23cd1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="23cd1-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="23cd1-106">Permission type</span></span>      | <span data-ttu-id="23cd1-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="23cd1-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="23cd1-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="23cd1-108">Delegated (work or school account)</span></span> | <span data-ttu-id="23cd1-109">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="23cd1-109">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="23cd1-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="23cd1-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="23cd1-111">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="23cd1-111">Not supported.</span></span>    |
|<span data-ttu-id="23cd1-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="23cd1-112">Application</span></span> | <span data-ttu-id="23cd1-113">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="23cd1-113">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="23cd1-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="23cd1-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groupLifecyclePolicies

```

## <a name="request-headers"></a><span data-ttu-id="23cd1-115">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="23cd1-115">Request headers</span></span>

| <span data-ttu-id="23cd1-116">名前</span><span class="sxs-lookup"><span data-stu-id="23cd1-116">Name</span></span> | <span data-ttu-id="23cd1-117">説明</span><span class="sxs-lookup"><span data-stu-id="23cd1-117">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="23cd1-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="23cd1-118">Authorization</span></span> | <span data-ttu-id="23cd1-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="23cd1-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="23cd1-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="23cd1-121">Content-Type</span></span>  | <span data-ttu-id="23cd1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="23cd1-122">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="23cd1-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="23cd1-123">Request body</span></span>
<span data-ttu-id="23cd1-124">要求本文で、[groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="23cd1-124">In the request body, supply a JSON representation of [plannerPlan](../resources/grouplifecyclepolicy.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="23cd1-125">応答</span><span class="sxs-lookup"><span data-stu-id="23cd1-125">Response</span></span>

<span data-ttu-id="23cd1-126">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="23cd1-126">If successful, this method returns a `201 Created` response code and [profilePhoto](../resources/grouplifecyclepolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="23cd1-127">例</span><span class="sxs-lookup"><span data-stu-id="23cd1-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="23cd1-128">要求</span><span class="sxs-lookup"><span data-stu-id="23cd1-128">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_grouplifecyclepolicy_from_group"
}-->
```http
POST https://graph.microsoft.com/v1.0/groupLifecyclePolicies
Content-type: application/json
Content-length: 125

{
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```
<span data-ttu-id="23cd1-129">要求本文で、[groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="23cd1-129">In the request body, supply a JSON representation of [plannerPlan](../resources/grouplifecyclepolicy.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="23cd1-130">応答</span><span class="sxs-lookup"><span data-stu-id="23cd1-130">Response</span></span>

<span data-ttu-id="23cd1-p103">注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="23cd1-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 174

{
  "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
  "groupLifetimeInDays": 100,
  "managedGroupTypes": "Selected",
  "alternateNotificationEmails": "admin@contoso.com"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->