# <a name="delete-outlook-category"></a><span data-ttu-id="94ab4-101">Outlook カテゴリを削除する</span><span class="sxs-lookup"><span data-stu-id="94ab4-101">Delete Outlook category</span></span>


<span data-ttu-id="94ab4-102">指定した [outlookCategory](../resources/outlookCategory.md) オブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="94ab4-102">Delete the specified [outlookCategory](../resources/outlookCategory.md) object.</span></span>

## <a name="permissions"></a><span data-ttu-id="94ab4-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="94ab4-103">Permissions</span></span>
<span data-ttu-id="94ab4-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94ab4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="94ab4-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="94ab4-106">Permission type</span></span>      | <span data-ttu-id="94ab4-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="94ab4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="94ab4-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="94ab4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="94ab4-109">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="94ab4-109">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="94ab4-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="94ab4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="94ab4-111">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="94ab4-111">MailboxSettings.ReadWrite</span></span>    |
|<span data-ttu-id="94ab4-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="94ab4-112">Application</span></span> | <span data-ttu-id="94ab4-113">MailboxSettings.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="94ab4-113">MailboxSettings.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="94ab4-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="94ab4-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/outlook/masterCategories/{id}
DELETE /users/{id|userPrincipalName}/outlook/masterCategories/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="94ab4-115">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="94ab4-115">Optional query parameters</span></span>
<span data-ttu-id="94ab4-116">このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](http://graph.microsoft.io/docs/overview/query_parameters)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="94ab4-116">This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="94ab4-117">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="94ab4-117">Request headers</span></span>
| <span data-ttu-id="94ab4-118">名前</span><span class="sxs-lookup"><span data-stu-id="94ab4-118">Name</span></span>      |<span data-ttu-id="94ab4-119">説明</span><span class="sxs-lookup"><span data-stu-id="94ab4-119">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="94ab4-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="94ab4-120">Authorization</span></span>  | <span data-ttu-id="94ab4-p102">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="94ab4-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="94ab4-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="94ab4-123">Request body</span></span>
<span data-ttu-id="94ab4-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="94ab4-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="94ab4-125">応答</span><span class="sxs-lookup"><span data-stu-id="94ab4-125">Response</span></span>

<span data-ttu-id="94ab4-p103">成功した場合、このメソッドは `204 No Content` 応答コードを返します。応答本文には何も返されません。</span><span class="sxs-lookup"><span data-stu-id="94ab4-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="94ab4-128">例</span><span class="sxs-lookup"><span data-stu-id="94ab4-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="94ab4-129">要求</span><span class="sxs-lookup"><span data-stu-id="94ab4-129">Request</span></span>
<span data-ttu-id="94ab4-130">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="94ab4-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_outlookcategory"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/outlook/masterCategories('4b1c2495-54c9-4a5e-90a2-0ab0b31987d8')
```
##### <a name="response"></a><span data-ttu-id="94ab4-131">応答</span><span class="sxs-lookup"><span data-stu-id="94ab4-131">Response</span></span>
<span data-ttu-id="94ab4-132">以下は、応答の例です。</span><span class="sxs-lookup"><span data-stu-id="94ab4-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "name": "delete_outlookcategory",
  "isEmpty": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete outlookCategory",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->