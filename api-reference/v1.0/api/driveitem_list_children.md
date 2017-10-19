---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: "フォルダーの内容を一覧表示する"
ms.openlocfilehash: e4c8f7b66333d739aeeaff9a8b92c0088d2fde0b
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2017
---
# <a name="list-children-of-a-driveitem"></a><span data-ttu-id="ffd98-102">driveItem の子を一覧表示する</span><span class="sxs-lookup"><span data-stu-id="ffd98-102">List children of a driveItem</span></span>

<span data-ttu-id="ffd98-103">DriveItem の**子**リレーションシップで [DriveItems](../resources/driveitem.md) のコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="ffd98-103">Return a collection of [DriveItems](../resources/driveitem.md) in the **children** relationship of a DriveItem.</span></span>

<span data-ttu-id="ffd98-104">NULL でない **folder** または **package** ファセットがある DriveItems は、1 つ以上の子 DriveItems を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="ffd98-104">DriveItems with a non-null **folder** or **package** facet can have one or more child DriveItems.</span></span>


## <a name="permissions"></a><span data-ttu-id="ffd98-105">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="ffd98-105">Permissions</span></span>

<span data-ttu-id="ffd98-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd98-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ffd98-108">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="ffd98-108">Permission type</span></span>      | <span data-ttu-id="ffd98-109">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="ffd98-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ffd98-110">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="ffd98-110">Delegated (work or school account)</span></span> | <span data-ttu-id="ffd98-111">Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All、Sites.Read.All、Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffd98-111">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="ffd98-112">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="ffd98-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ffd98-113">Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffd98-113">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="ffd98-114">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="ffd98-114">Application</span></span> | <span data-ttu-id="ffd98-115">Files.Read.All、Files.ReadWrite.All、Sites.Read.All、Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffd98-115">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ffd98-116">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="ffd98-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
GET /groups/{group-id}/drive/items/{item-id}/children
GET /me/drive/items/{item-id}/children
GET /sites/{site-id}/drive/items/{item-id}/children
GET /users/{user-id}/drive/items/{item-id}/children
```

## <a name="optional-query-parameters"></a><span data-ttu-id="ffd98-117">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="ffd98-117">Optional query parameters</span></span>

<span data-ttu-id="ffd98-118">このメソッドは、応答をカスタマイズするための `$expand`、`$select`、`$skipToken`、`$top`、`$orderby` の [OData クエリ パラメーター](../../../concepts/query_parameters.md)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ffd98-118">This method supports the `$expand`, `$select`, `$skipToken`, `$top` and `$orderby` [OData query parameters](../../../concepts/query_parameters.md) to customize the response.</span></span>

### <a name="optional-request-headers"></a><span data-ttu-id="ffd98-119">オプションの要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="ffd98-119">Optional request headers</span></span>

| <span data-ttu-id="ffd98-120">ヘッダー名</span><span class="sxs-lookup"><span data-stu-id="ffd98-120">Header name</span></span>     | <span data-ttu-id="ffd98-121">値</span><span class="sxs-lookup"><span data-stu-id="ffd98-121">Value</span></span> | <span data-ttu-id="ffd98-122">説明</span><span class="sxs-lookup"><span data-stu-id="ffd98-122">Description</span></span>                                                                                                                                              |
|:----------------|:------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd98-123">_if-none-match_</span><span class="sxs-lookup"><span data-stu-id="ffd98-123">_if-none-match_</span></span> | <span data-ttu-id="ffd98-124">etag</span><span class="sxs-lookup"><span data-stu-id="ffd98-124">etag</span></span>  | <span data-ttu-id="ffd98-125">この要求ヘッダーが含まれている場合、指定された eTag (または cTag) がファイルの現在のタグに一致すると、`HTTP 304 Not Modified` 応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="ffd98-125">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="examples"></a><span data-ttu-id="ffd98-126">例</span><span class="sxs-lookup"><span data-stu-id="ffd98-126">Examples</span></span>

### <a name="list-children-in-the-root-of-the-current-users-drive"></a><span data-ttu-id="ffd98-127">現在のユーザーのドライブのルートの子を一覧表示する</span><span class="sxs-lookup"><span data-stu-id="ffd98-127">List children in the root of the current user's drive</span></span>

<span data-ttu-id="ffd98-128">ドライブのルートのファイルを取得するには、ドライブ上の `root` リレーションシップを使用して、子のリレーションシップにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ffd98-128">To retrieve files in the root of the drive, use the `root` relationship on the drive, then access the children relationship.</span></span>

<!-- { "blockType": "request", "name": "list-children-root", "scopes": "files.read" } -->

```http
GET /me/drive/root/children
```


### <a name="list-children-of-a-driveitem-with-a-known-id"></a><span data-ttu-id="ffd98-129">既知の ID を持つ DriveItem の子を一覧表示する</span><span class="sxs-lookup"><span data-stu-id="ffd98-129">List children of a DriveItem with a known ID</span></span>

<span data-ttu-id="ffd98-130">ドライブのルートのファイルを取得するには、ドライブ上の `root` リレーションシップを使用して、子のリレーションシップにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="ffd98-130">To retrieve files in the root of the drive, use the `root` relationship on the drive, then access the children relationship.</span></span>

<!-- { "blockType": "request", "name": "list-children", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/items/{item-id}/children
```

### <a name="list-children-of-a-driveitem-with-a-known-path"></a><span data-ttu-id="ffd98-131">既知のパスを持つ DriveItem の子を一覧表示する</span><span class="sxs-lookup"><span data-stu-id="ffd98-131">List children of a DriveItem with a known path</span></span>

<!-- { "blockType": "request", "name": "list-children-from-path", "scopes": "files.read" } -->

```http
GET /drives/{drive-id}/root:/{path-relative-to-root}:/children
```

## <a name="response"></a><span data-ttu-id="ffd98-132">応答</span><span class="sxs-lookup"><span data-stu-id="ffd98-132">Response</span></span>

<span data-ttu-id="ffd98-133">成功すると、このメソッドはターゲット アイテムの子コレクション内にあるアイテムの一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="ffd98-133">If successful, this method returns the list of items in the children collection of the target item.</span></span>
<span data-ttu-id="ffd98-134">子コレクションは、[driveItem][item-resource] リソースで構成されます。</span><span class="sxs-lookup"><span data-stu-id="ffd98-134">The children collection will be composed of [driveItem][item-resource] resources.</span></span>

<!-- { "blockType": "response", 
       "@odata.type": "Collection(microsoft.graph.driveItem)", 
       "truncated": true,
       "name": [ "list-children-root", "list-children", "list-children-from-path" ] } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048, "file": {} },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ],
  "@odata.nextLink": "https://..."
}
```

<span data-ttu-id="ffd98-135">**注:**コレクションが既定のページ サイズ (200 アイテム) を超えた場合は、応答で **@odata.nextLink** プロパティが返され、より多くのアイテムが使用できることが示されます。また、アイテムの次のページの要求 URL も提供されます。</span><span class="sxs-lookup"><span data-stu-id="ffd98-135">**Note:** If a collection exceeds the default page size (200 items), the **@odata.nextLink** property is returned in the response to indicate more items are available and provide the request URL for the next page of items.</span></span>

<span data-ttu-id="ffd98-136">ページ サイズは[オプションのクエリ文字列パラメーター](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)で制御できます。</span><span class="sxs-lookup"><span data-stu-id="ffd98-136">You can control the page size through [optional query string parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)</span></span>

### <a name="error-responses"></a><span data-ttu-id="ffd98-137">エラー応答</span><span class="sxs-lookup"><span data-stu-id="ffd98-137">Error responses</span></span>

<span data-ttu-id="ffd98-138">エラーがどのように返されるかについては、「[エラー応答][error-response]」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ffd98-138">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md
[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "List the children of an item.",
  "keywords": "list,children,collection",
  "section": "documentation",
  "tocPath": "Items/List children"
} -->