# <a name="create-outlook-category"></a><span data-ttu-id="ade2d-101">Outlook カテゴリを作成する</span><span class="sxs-lookup"><span data-stu-id="ade2d-101">Create Outlook category</span></span>


<span data-ttu-id="ade2d-102">ユーザーのマスター カテゴリ リスト内に [outlookCategory](../resources/outlookCategory.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ade2d-102">Create an [outlookCategory](../resources/outlookCategory.md) object in the user's master list of categories.</span></span>

## <a name="permissions"></a><span data-ttu-id="ade2d-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="ade2d-103">Permissions</span></span>
<span data-ttu-id="ade2d-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ade2d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ade2d-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="ade2d-106">Permission type</span></span>      | <span data-ttu-id="ade2d-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="ade2d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ade2d-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="ade2d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ade2d-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ade2d-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="ade2d-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="ade2d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ade2d-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ade2d-111">MailboxSettings.ReadWrite</span></span>   |
|<span data-ttu-id="ade2d-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ade2d-112">Application</span></span> | <span data-ttu-id="ade2d-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ade2d-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ade2d-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="ade2d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/outlook/masterCategories
POST /users/{id|userPrincipalName}/outlook/masterCategories
```
## <a name="request-headers"></a><span data-ttu-id="ade2d-115">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="ade2d-115">Request headers</span></span>
| <span data-ttu-id="ade2d-116">名前</span><span class="sxs-lookup"><span data-stu-id="ade2d-116">Name</span></span>       | <span data-ttu-id="ade2d-117">説明</span><span class="sxs-lookup"><span data-stu-id="ade2d-117">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="ade2d-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="ade2d-118">Authorization</span></span>  | <span data-ttu-id="ade2d-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="ade2d-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="ade2d-121">要求本文</span><span class="sxs-lookup"><span data-stu-id="ade2d-121">Request body</span></span>
<span data-ttu-id="ade2d-122">要求本文に、[outlookCategory](../resources/outlookCategory.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="ade2d-122">In the request body, supply a JSON representation of [plannerTask](../resources/outlookCategory.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="ade2d-123">応答</span><span class="sxs-lookup"><span data-stu-id="ade2d-123">Response</span></span>

<span data-ttu-id="ade2d-124">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文に [outlookCategory](../resources/outlookCategory.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="ade2d-124">If successful, this method returns `201 Created` response code and the new [page](../resources/outlookCategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ade2d-125">例</span><span class="sxs-lookup"><span data-stu-id="ade2d-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ade2d-126">要求</span><span class="sxs-lookup"><span data-stu-id="ade2d-126">Request</span></span>
<span data-ttu-id="ade2d-127">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="ade2d-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_outlookcategory_from_outlookuser"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/outlook/masterCategories
Content-type: application/json
Content-Length: 70

{
      "displayName":"Project expenses",
      "color":"preset9"
}
```
<span data-ttu-id="ade2d-128">要求本文に、[outlookCategory](../resources/outlookCategory.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="ade2d-128">In the request body, supply a JSON representation of [plannerTask](../resources/outlookCategory.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="ade2d-129">応答</span><span class="sxs-lookup"><span data-stu-id="ade2d-129">Response</span></span>
<span data-ttu-id="ade2d-p103">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="ade2d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.outlookCategory"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 250

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('8ae6f565-0d7f-4ead-853e-7db94c912a1f')/outlook/masterCategories/$entity",
  "id":"bac262b7-485d-4739-b436-e31467d64fac",
  "displayName":"Project expenses",
  "color":"preset9"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->