# <a name="get-user"></a><span data-ttu-id="895c6-101">Get user</span><span class="sxs-lookup"><span data-stu-id="895c6-101">Get user</span></span>

<span data-ttu-id="895c6-102">この **educationUser** に対応する単純なディレクトリ **user** を取得します。</span><span class="sxs-lookup"><span data-stu-id="895c6-102">Retrieve the simple directory **user** that corresponds to this **educationUser**.</span></span>

><span data-ttu-id="895c6-103">**注:** 委任されたトークンを使用した場合、メンバーは自分の学校に関する情報以外を参照できません。</span><span class="sxs-lookup"><span data-stu-id="895c6-103">**Note:** If the delegated token is used, members can only see information about their own schools.</span></span> <span data-ttu-id="895c6-104">この場合は `...beta/education/me/schools` リソースを使用してください。</span><span class="sxs-lookup"><span data-stu-id="895c6-104">Use the `...beta/education/me/schools` resource in this case.</span></span>

## <a name="permissions"></a><span data-ttu-id="895c6-105">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="895c6-105">Permissions</span></span>
<span data-ttu-id="895c6-106">この API を呼び出すには、アクセス許可の組み合わせが必要です。</span><span class="sxs-lookup"><span data-stu-id="895c6-106">A combination of permissions is required to call this API.</span></span> <span data-ttu-id="895c6-107">アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="895c6-107">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="895c6-108">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="895c6-108">Permission type</span></span>      | <span data-ttu-id="895c6-109">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="895c6-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="895c6-110">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="895c6-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="895c6-111">One from EduRoster.ReadBasic、EduRoster.Read、EduRoster.Write plus either Directory.Read.All or User.Read</span><span class="sxs-lookup"><span data-stu-id="895c6-111">One from EduRoster.ReadBasic, EduRoster.Read, EduRoster.Write plus either Directory.Read.All or User.Read</span></span>|
|<span data-ttu-id="895c6-112">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="895c6-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="895c6-113">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="895c6-113">Not supported.</span></span>  |
|<span data-ttu-id="895c6-114">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="895c6-114">Application</span></span> | <span data-ttu-id="895c6-115">EduRoster.Read.All、EduRoster.ReadWrite.All plus Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="895c6-115">EduRoster.Read.All, EduRoster.ReadWrite.All plus Directory.Read.All</span></span>| 

## <a name="http-request"></a><span data-ttu-id="895c6-116">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="895c6-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /education/me/user
GET /education/users/{id}/user
```
## <a name="request-headers"></a><span data-ttu-id="895c6-117">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="895c6-117">Request headers</span></span>
| <span data-ttu-id="895c6-118">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="895c6-118">Header</span></span>       | <span data-ttu-id="895c6-119">値</span><span class="sxs-lookup"><span data-stu-id="895c6-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="895c6-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="895c6-120">Authorization</span></span>  | <span data-ttu-id="895c6-p103">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="895c6-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="895c6-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="895c6-123">Request body</span></span>
<span data-ttu-id="895c6-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="895c6-124">Do not supply a request body for this method.</span></span>
## <a name="response"></a><span data-ttu-id="895c6-125">応答</span><span class="sxs-lookup"><span data-stu-id="895c6-125">Response</span></span>
<span data-ttu-id="895c6-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [user](../resources/user.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="895c6-126">If successful, this method returns a `200 OK` response code and [user](../resources/user.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="895c6-127">例</span><span class="sxs-lookup"><span data-stu-id="895c6-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="895c6-128">要求</span><span class="sxs-lookup"><span data-stu-id="895c6-128">Request</span></span>
<span data-ttu-id="895c6-129">要求の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="895c6-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_user"
}-->
```http
GET https://graph.microsoft.com/v1.0/education/me/user
```
##### <a name="response"></a><span data-ttu-id="895c6-130">応答</span><span class="sxs-lookup"><span data-stu-id="895c6-130">Response</span></span>
<span data-ttu-id="895c6-131">応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="895c6-131">The following is an example of the response.</span></span> 

><span data-ttu-id="895c6-p104">**注:** 読みやすくするために、ここに示す応答オブジェクトは短くされている場合があります。実際の呼び出しからは、すべてのプロパティが返されます。</span><span class="sxs-lookup"><span data-stu-id="895c6-p104">**Note:** The response object shown here might be shortened for readability. All the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.user",
  "isCollection": false
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 491

{
  "businessPhones": [
       "businessPhones-value"
   ],
   "displayName": "displayName-value",
   "givenName": "givenName-value",
   "jobTitle": "jobTitle-value",
   "mail": "mail-value",
   "mobilePhone": "mobilePhone-value",
   "officeLocation": "officeLocation-value",
   "preferredLanguage": "preferredLanguage-value",
   "surname": "surname-value",
   "userPrincipalName": "userPrincipalName-value",
   "id": "id-value"
}
```

<!-- uuid: FC4AAF57-A0ED-4899-B104-A8B89B72AD5A
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->