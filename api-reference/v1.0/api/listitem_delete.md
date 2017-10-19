---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: "SharePoint リストからエントリを削除する"
ms.openlocfilehash: d16e90c44fcf2a51dae4cc91134d512807c333f6
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2017
---
# <a name="delete-an-item-from-a-list"></a><span data-ttu-id="66bf7-102">リストからアイテムを削除する</span><span class="sxs-lookup"><span data-stu-id="66bf7-102">Deletes an item from a list</span></span>

<span data-ttu-id="66bf7-103">[list][] からアイテムを削除します。</span><span class="sxs-lookup"><span data-stu-id="66bf7-103">Removes an item from a  [collection][].</span></span>

[list]: ../resources/list.md

## <a name="permissions"></a><span data-ttu-id="66bf7-105">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="66bf7-105">Permissions</span></span>

<span data-ttu-id="66bf7-106">アイテムを削除するには、削除するアイテムへの書き込みアクセス権がユーザーに付与されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="66bf7-106">To delete an item, the user must have granted the application write access to the item to be deleted.</span></span>

<span data-ttu-id="66bf7-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66bf7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="66bf7-109">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="66bf7-109">Permission type</span></span>      | <span data-ttu-id="66bf7-110">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="66bf7-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="66bf7-111">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="66bf7-111">Delegated (work or school account)</span></span> | <span data-ttu-id="66bf7-112">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66bf7-112">Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="66bf7-113">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="66bf7-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="66bf7-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="66bf7-114">Not supported.</span></span>    |
|<span data-ttu-id="66bf7-115">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="66bf7-115">Application</span></span> | <span data-ttu-id="66bf7-116">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="66bf7-116">Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="66bf7-117">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="66bf7-117">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
DELETE https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="optional-request-headers"></a><span data-ttu-id="66bf7-118">オプションの要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="66bf7-118">Optional request headers</span></span>

| <span data-ttu-id="66bf7-119">名前</span><span class="sxs-lookup"><span data-stu-id="66bf7-119">Name</span></span>       | <span data-ttu-id="66bf7-120">値</span><span class="sxs-lookup"><span data-stu-id="66bf7-120">Value</span></span> | <span data-ttu-id="66bf7-121">説明</span><span class="sxs-lookup"><span data-stu-id="66bf7-121">Description</span></span>
|:-----------|:------|:--------------------------------------------------------
| <span data-ttu-id="66bf7-122">_if-match_</span><span class="sxs-lookup"><span data-stu-id="66bf7-122">_if-match_</span></span> | <span data-ttu-id="66bf7-123">etag</span><span class="sxs-lookup"><span data-stu-id="66bf7-123">etag</span></span>  | <span data-ttu-id="66bf7-124">この要求ヘッダーが含まれていて、指定された eTag がアイテムの現在のタグに一致しない場合には、`412 Precondition Failed` 応答が返され、アイテムは削除されません。</span><span class="sxs-lookup"><span data-stu-id="66bf7-124">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>

## <a name="request-body"></a><span data-ttu-id="66bf7-125">要求本文</span><span class="sxs-lookup"><span data-stu-id="66bf7-125">Request body</span></span>

<span data-ttu-id="66bf7-126">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="66bf7-126">Do not supply a request body with this method.</span></span>

## <a name="example"></a><span data-ttu-id="66bf7-127">例</span><span class="sxs-lookup"><span data-stu-id="66bf7-127">Example</span></span>

<!-- { "blockType": "request", "name": "delete-item", "scopes": "files.readwrite" } -->

```http
DELETE https://graph.microsoft.com/beta/sites/{site-id}/lists/{list-id}/items/{item-id}
```

## <a name="response"></a><span data-ttu-id="66bf7-128">応答</span><span class="sxs-lookup"><span data-stu-id="66bf7-128">Response</span></span>

<span data-ttu-id="66bf7-129">成功した場合、この呼び出しはリソースが削除され返すものがなかったことを示す `204 No Content` 応答を返します。</span><span class="sxs-lookup"><span data-stu-id="66bf7-129">If successful, this call returns a `204 No Content` response to indicate that resource was deleted and there was nothing to return.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "ListItem/Delete"
} -->