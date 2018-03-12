# <a name="remove-educationuser-from-an-educationschool"></a><span data-ttu-id="4c5e8-101">educationSchool から educationUser を削除する</span><span class="sxs-lookup"><span data-stu-id="4c5e8-101">Remove educationUser from an educationSchool</span></span>

<span data-ttu-id="4c5e8-102">学校からユーザーを削除します。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-102">Delete a user from a school.</span></span>

## <a name="permissions"></a><span data-ttu-id="4c5e8-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="4c5e8-103">Permissions</span></span>
<span data-ttu-id="4c5e8-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="4c5e8-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="4c5e8-106">Permission type</span></span>      | <span data-ttu-id="4c5e8-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="4c5e8-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4c5e8-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="4c5e8-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="4c5e8-109">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-109">Not supported.</span></span>  |
|<span data-ttu-id="4c5e8-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="4c5e8-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="4c5e8-111">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-111">Not supported.</span></span>  |
|<span data-ttu-id="4c5e8-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4c5e8-112">Application</span></span> | <span data-ttu-id="4c5e8-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4c5e8-113">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="4c5e8-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="4c5e8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/schools/<id>/users/{userId}/$ref
```
## <a name="request-headers"></a><span data-ttu-id="4c5e8-115">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4c5e8-115">Request headers</span></span>
| <span data-ttu-id="4c5e8-116">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4c5e8-116">Header</span></span>       | <span data-ttu-id="4c5e8-117">値</span><span class="sxs-lookup"><span data-stu-id="4c5e8-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4c5e8-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="4c5e8-118">Authorization</span></span>  | <span data-ttu-id="4c5e8-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4c5e8-121">要求本文</span><span class="sxs-lookup"><span data-stu-id="4c5e8-121">Request body</span></span>
<span data-ttu-id="4c5e8-122">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-122">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="4c5e8-123">応答</span><span class="sxs-lookup"><span data-stu-id="4c5e8-123">Response</span></span>
<span data-ttu-id="4c5e8-124">成功した場合、このメソッドは `204 No Content` 応答コードと空の応答本文を返します。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-124">If successful, this method returns a `204 No Content` response code and an event object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4c5e8-125">例</span><span class="sxs-lookup"><span data-stu-id="4c5e8-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4c5e8-126">要求</span><span class="sxs-lookup"><span data-stu-id="4c5e8-126">Request</span></span>
<span data-ttu-id="4c5e8-127">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_educationclass_from_educationschool"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/schools/10001/users/13006
```

##### <a name="response"></a><span data-ttu-id="4c5e8-128">応答</span><span class="sxs-lookup"><span data-stu-id="4c5e8-128">Response</span></span>
<span data-ttu-id="4c5e8-129">応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4c5e8-129">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationClass"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->