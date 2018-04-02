# <a name="list-grouplifecyclepolicies"></a><span data-ttu-id="c3971-101">List groupLifecyclePolicies</span><span class="sxs-lookup"><span data-stu-id="c3971-101">List groupLifecyclePolicies</span></span>

<span data-ttu-id="c3971-102">すべての [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md) を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="c3971-102">List all the [groupLifecyclePolicies](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c3971-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="c3971-103">Permissions</span></span>

<span data-ttu-id="c3971-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3971-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>


|<span data-ttu-id="c3971-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="c3971-106">Permission type</span></span>      | <span data-ttu-id="c3971-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="c3971-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c3971-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="c3971-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c3971-109">Directory.Read.All、Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3971-109">Directory.Read.All, Directory.ReadWrite.All</span></span> |
|<span data-ttu-id="c3971-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="c3971-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c3971-111">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c3971-111">Not supported.</span></span>    |
|<span data-ttu-id="c3971-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c3971-112">Application</span></span> | <span data-ttu-id="c3971-113">Directory.Read.All、Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3971-113">Directory.Read.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c3971-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="c3971-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groupLifecyclePolicies
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c3971-115">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="c3971-115">Optional query parameters</span></span>
<span data-ttu-id="c3971-116">このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](http://graph.microsoft.io/docs/overview/query_parameters)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="c3971-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c3971-117">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c3971-117">Request headers</span></span>
| <span data-ttu-id="c3971-118">名前</span><span class="sxs-lookup"><span data-stu-id="c3971-118">Name</span></span> | <span data-ttu-id="c3971-119">説明</span><span class="sxs-lookup"><span data-stu-id="c3971-119">Description</span></span> |
|:----------|:----------|
| <span data-ttu-id="c3971-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3971-120">Authorization</span></span> | <span data-ttu-id="c3971-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="c3971-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c3971-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="c3971-123">Request body</span></span>
<span data-ttu-id="c3971-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="c3971-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c3971-125">応答</span><span class="sxs-lookup"><span data-stu-id="c3971-125">Response</span></span>

<span data-ttu-id="c3971-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="c3971-126">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/grouplifecyclepolicy.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c3971-127">例</span><span class="sxs-lookup"><span data-stu-id="c3971-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c3971-128">要求</span><span class="sxs-lookup"><span data-stu-id="c3971-128">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_grouplifecyclepolicy"
}-->
```http
GET https://graph.microsoft.com/v1.0/groupLifecyclePolicies
```
##### <a name="response"></a><span data-ttu-id="c3971-129">応答</span><span class="sxs-lookup"><span data-stu-id="c3971-129">Response</span></span>

<span data-ttu-id="c3971-p103">注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="c3971-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.groupLifecyclePolicy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 223

{
  "value": [
    {
      "id": "ffffffff-ffff-ffff-ffff-ffffffffffff",
      "groupLifetimeInDays": 100,
      "managedGroupTypes": "Selected",
      "alternateNotificationEmails": "admin@contoso.com"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List groupLifecyclePolicies",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->