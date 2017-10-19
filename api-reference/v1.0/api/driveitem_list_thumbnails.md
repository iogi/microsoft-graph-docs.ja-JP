---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: "ファイルまたはフォルダーのサムネイルを取得する"
ms.openlocfilehash: 864765898955d0a690ab85dc0be9761a7a9d1856
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2017
---
# <a name="list-thumbnails-for-a-driveitem"></a><span data-ttu-id="20056-102">DriveItem のサムネイルを一覧表示する</span><span class="sxs-lookup"><span data-stu-id="20056-102">List thumbnails for a DriveItem</span></span>

<span data-ttu-id="20056-103">[DriveItem](../resources/driveitem.md) リソースの [ThumbnailSet](../resources/thumbnailset.md) リソースのコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="20056-103">Retrieve a collection of [ThumbnailSet](../resources/thumbnailset.md) resources for a [DriveItem](../resources/driveitem.md) resource.</span></span>

<span data-ttu-id="20056-p101">DriveItem はゼロ以上の [ThumbnailSet](../resources/thumbnailset.md) リソースで表すことができます。各 **thumbnailSet** は 1 つ以上の[**サムネイル**](../resources/thumbnail.md) オブジェクトを持つことができ、そのオブジェクトはアイテムを表すイメージです。たとえば、**thumbnailSet** には `small`、`medium`、`large` など、一般的な**サムネイル** オブジェクトが含まれます。</span><span class="sxs-lookup"><span data-stu-id="20056-p101">A DriveItem can be represented by zero or more [ThumbnailSet](../resources/thumbnailset.md) resources. Each **thumbnailSet** can have one or more [**thumbnail**](../resources/thumbnail.md) objects, which are images that represent the item. For example, a **thumbnailSet** may include **thumbnail** objects, such as common ones including `small`, `medium`, or `large`.</span></span>

<span data-ttu-id="20056-p102">OneDrive 上でサムネイルを操作する方法はたくさんあります。次に、最も一般的なものを示します。</span><span class="sxs-lookup"><span data-stu-id="20056-p102">There are many ways to work with thumbnails on OneDrive. Here are the most common ones:</span></span>

* <span data-ttu-id="20056-109">アイテムの利用可能なサムネイルを列挙する</span><span class="sxs-lookup"><span data-stu-id="20056-109">Enumerate available thumbnails for an item</span></span>
* <span data-ttu-id="20056-110">アイテムの 1 つのサムネイルを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-110">Retrieve a single thumbnail for an item</span></span>
* <span data-ttu-id="20056-111">サムネイルのコンテンツを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-111">Retrieve thumbnail content</span></span>
* <span data-ttu-id="20056-112">1 つの要求で複数のアイテムのサムネイルを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-112">Retrieve thumbnails for multiple items in a single request</span></span>
* <span data-ttu-id="20056-113">カスタムのサムネイル サイズを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-113">Retrieve custom thumbnail sizes</span></span>
* <span data-ttu-id="20056-114">アイテムのカスタム サムネイルをアップロードする</span><span class="sxs-lookup"><span data-stu-id="20056-114">Upload a custom thumbnail for an item</span></span>
* <span data-ttu-id="20056-115">カスタムのアップロード済みサムネイルが存在するかどうかを確認する</span><span class="sxs-lookup"><span data-stu-id="20056-115">Determine if a custom uploaded thumbnail exists</span></span>

## <a name="permissions"></a><span data-ttu-id="20056-116">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="20056-116">Permissions</span></span>

<span data-ttu-id="20056-p103">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20056-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="20056-119">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="20056-119">Permission type</span></span>      | <span data-ttu-id="20056-120">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="20056-120">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="20056-121">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="20056-121">Delegated (work or school account)</span></span> | <span data-ttu-id="20056-122">Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All、Sites.Read.All、Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="20056-122">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="20056-123">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="20056-123">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="20056-124">Files.Read、Files.ReadWrite、Files.Read.All、Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="20056-124">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="20056-125">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="20056-125">Application</span></span> | <span data-ttu-id="20056-126">Files.Read.All、Files.ReadWrite.All、Sites.Read.All、Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="20056-126">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="20056-127">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="20056-127">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /drives/{drive-id}/items/{item-id}/thumbnails
GET /groups/{group-id}/drive/items/{item-id}/thumbnails
GET /me/drive/items/{item-id}/thumbnails
GET /sites/{site-id}/drive/items/{item-id}/thumbnails
GET /users/{user-id}/drive/items/{item-id}/thumbnails
```

## <a name="optional-query-parameters"></a><span data-ttu-id="20056-128">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="20056-128">Optional query parameters</span></span>

<span data-ttu-id="20056-129">このメソッドは、応答をカスタマイズするための `$select` の [OData クエリ パラメーター](../../../concepts/query_parameters.md)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="20056-129">This method supports the `$select` [OData puery parameter](../../../concepts/query_parameters.md) to customize the response.</span></span>

## <a name="response"></a><span data-ttu-id="20056-130">応答</span><span class="sxs-lookup"><span data-stu-id="20056-130">Response</span></span>

<span data-ttu-id="20056-131">成功した場合、このメソッドは応答本文で `200 OK` 応答コードと [ThumbnailSet](../resources/thumbnailset.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="20056-131">If successful, this method returns a `200 OK` response code and collection of [ThumbnailSet](../resources/thumbnailset.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="20056-132">例</span><span class="sxs-lookup"><span data-stu-id="20056-132">Example</span></span>

<span data-ttu-id="20056-133">次は、現在のユーザーの OneDrive 内のアイテムで使用可能なサムネイルを取得する要求の例です。</span><span class="sxs-lookup"><span data-stu-id="20056-133">Here is an example of the request which retrieves available thumbnails for an item in the current user's OneDrive.</span></span>

<!-- { "blockType": "request", "name": "enum-item-thumbnails", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails
```

<span data-ttu-id="20056-134">この要求では、そのアイテムで使用可能な **thumbnailSets** の配列が返されます。</span><span class="sxs-lookup"><span data-stu-id="20056-134">This returns an array of available **thumbnailSets** for the item.</span></span> <span data-ttu-id="20056-135">ドライブにあるすべてのアイテムは、0 個以上のサムネイルを保持できます。</span><span class="sxs-lookup"><span data-stu-id="20056-135">Any item in OneDrive can have zero or more thumbnails.</span></span>

<span data-ttu-id="20056-136">**注:** _select_ クエリ文字列パラメーターを使用すると、**ThumbnailSet** で返されるサムネイルのサイズを制御できます。</span><span class="sxs-lookup"><span data-stu-id="20056-136">**Note:** You can use the _select_ query string parameter to control which thumbnail sizes are returned in the **ThumbnailSet**.</span></span>
<span data-ttu-id="20056-137">たとえば、`/thumbnails?select=medium` では、中サイズのサムネイルのみを取得します。</span><span class="sxs-lookup"><span data-stu-id="20056-137">For example, `/thumbnails?select=medium` retrieves only the medium sized thumbnails.</span></span>


### <a name="response"></a><span data-ttu-id="20056-138">応答</span><span class="sxs-lookup"><span data-stu-id="20056-138">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "0",
      "small": { "height": 64, "width": 96, "url": "https://sn3302files..."},
      "medium": { "height": 117, "width": 176, "url": "https://sn3302files..."},
      "large": { "height": 533, "width": 800, "url": "https://sn3302files..."}
    }
  ]
}
```

## <a name="get-a-single-thumbnail"></a><span data-ttu-id="20056-139">1 つのサムネイルを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-139">Retrieve a single thumbnail</span></span>

<span data-ttu-id="20056-140">1 つのサムネイルとサイズのメタデータを、要求で直接アドレス指定 (特定して) して取得します。</span><span class="sxs-lookup"><span data-stu-id="20056-140">Retrieve the metadata for a single thumbnail and size by addressing it directly in a request.</span></span>

### <a name="http-request"></a><span data-ttu-id="20056-141">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="20056-141">HTTP request</span></span>

<!-- { "blockType": "request", "name": "get-one-thumbnail", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}
```

### <a name="path-parameters"></a><span data-ttu-id="20056-142">パス パラメーター</span><span class="sxs-lookup"><span data-stu-id="20056-142">Path parameters</span></span>

| <span data-ttu-id="20056-143">名前</span><span class="sxs-lookup"><span data-stu-id="20056-143">Name</span></span>         | <span data-ttu-id="20056-144">型</span><span class="sxs-lookup"><span data-stu-id="20056-144">Type</span></span>   | <span data-ttu-id="20056-145">説明</span><span class="sxs-lookup"><span data-stu-id="20056-145">Description</span></span>                                                                              |
|:-------------|:-------|:-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20056-146">**item-id**</span><span class="sxs-lookup"><span data-stu-id="20056-146">**item-id**</span></span>  | <span data-ttu-id="20056-147">string</span><span class="sxs-lookup"><span data-stu-id="20056-147">string</span></span> | <span data-ttu-id="20056-148">参照されるアイテムの一意識別子。</span><span class="sxs-lookup"><span data-stu-id="20056-148">The unique identifier for the item referenced.</span></span>                                           |
| <span data-ttu-id="20056-149">**thumb-id**</span><span class="sxs-lookup"><span data-stu-id="20056-149">**thumb-id**</span></span> | <span data-ttu-id="20056-150">number</span><span class="sxs-lookup"><span data-stu-id="20056-150">number</span></span> | <span data-ttu-id="20056-151">サムネイルのインデックス (通常 0-4)。</span><span class="sxs-lookup"><span data-stu-id="20056-151">The index of the thumbnail, usually 0-4.</span></span> <span data-ttu-id="20056-152">カスタム サムネイルがある場合は、そのインデックスは 0 になります。</span><span class="sxs-lookup"><span data-stu-id="20056-152">If there is a custom thumbnail, its index is 0.</span></span> |
| <span data-ttu-id="20056-153">**size**</span><span class="sxs-lookup"><span data-stu-id="20056-153">**size**</span></span>     | <span data-ttu-id="20056-154">string</span><span class="sxs-lookup"><span data-stu-id="20056-154">string</span></span> | <span data-ttu-id="20056-155">要求されるサムネイルのサイズ。</span><span class="sxs-lookup"><span data-stu-id="20056-155">The size of the thumbnail requested.</span></span> <span data-ttu-id="20056-156">これは、後述する標準サイズか、カスタム サイズのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="20056-156">This can be one of the standard sizes listed below or a custom size.</span></span> |

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.thumbnail" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "width": 100,
  "height": 100,
  "url": "http://onedrive.com/asd123a/asdjlkasjdkasdjlk.jpg"
}
```

## <a name="retrieve-thumbnail-binary-content"></a><span data-ttu-id="20056-157">サムネイルのバイナリ コンテンツを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-157">Retrieve thumbnail content</span></span>

<span data-ttu-id="20056-158">サムネイルの **content** プロパティを要求することにより、サムネイルのコンテンツを直接取得できます。</span><span class="sxs-lookup"><span data-stu-id="20056-158">You can directly retrieve the content of the thumbnail by requesting the **content** property of the thumbnail.</span></span>

### <a name="http-request"></a><span data-ttu-id="20056-159">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="20056-159">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-content", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails/{thumb-id}/{size}/content
```

### <a name="response"></a><span data-ttu-id="20056-160">応答</span><span class="sxs-lookup"><span data-stu-id="20056-160">Response</span></span>

<span data-ttu-id="20056-161">サービスは、サムネイルの URL へのリダイレクトで応答します。</span><span class="sxs-lookup"><span data-stu-id="20056-161">The service responds with a redirect to the thumbnail URL.</span></span>

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 302 Found
Location: https://b0mpua-by3301.files.1drv.com/y23vmagahszhxzlcvhasdhasghasodfi
```

<span data-ttu-id="20056-162">サムネイル URL はキャッシュ対応です。</span><span class="sxs-lookup"><span data-stu-id="20056-162">Thumbnail URLs are cache-safe.</span></span> <span data-ttu-id="20056-163">この URL は、新しいサムネイルの生成を要求する方法でアイテムを変更する場合に変更されます。</span><span class="sxs-lookup"><span data-stu-id="20056-163">The URL will change, if the item changes in a way that requires a new thumbnail to be generated.</span></span>


## <a name="getting-thumbnails-while-listing-driveitems"></a><span data-ttu-id="20056-164">DriveItems を一覧表示する際にサムネイルを取得する</span><span class="sxs-lookup"><span data-stu-id="20056-164">Getting thumbnails while listing DriveItems</span></span>

<span data-ttu-id="20056-165">表示する DriveItem リソースのリストを取得する場合、_$expand_ クエリ文字列パラメーターを使用して、それらのリソースのサムネイルも含めることができます。</span><span class="sxs-lookup"><span data-stu-id="20056-165">If you are retrieving a list of DriveItem resources to display, you can use the _$expand_ query string parameter to also include the thumbnails for those resources.</span></span>
<span data-ttu-id="20056-166">これによりアプリは、複数の要求を実行することなく、サムネイルとアイテムを 1 つの要求で取得することができます。</span><span class="sxs-lookup"><span data-stu-id="20056-166">This enables your app to retrieve thumbnails and items in a single request, instead of issuing many requests.</span></span>

### <a name="http-request"></a><span data-ttu-id="20056-167">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="20056-167">HTTP request</span></span>

<!-- { "blockType": "request", "name":"get-thumbnail-while-listing", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/children?$expand=thumbnails
```

### <a name="response"></a><span data-ttu-id="20056-168">応答</span><span class="sxs-lookup"><span data-stu-id="20056-168">Response</span></span>

<span data-ttu-id="20056-169">サービスは、DriveItems とそのサムネイルのリストで応答します。</span><span class="sxs-lookup"><span data-stu-id="20056-169">The service responses with the list of DriveItems and their thumbnails.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.driveItem)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "id": "182331E8-2788-4932-B52A-A6550577043F",
      "name": "my photo.jpg",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    },
    {
      "id": "2D223953-A56B-4D9B-ADF3-13E7820673A2",
      "name": "presentation.pptx",
      "thumbnails": [
        {
          "small": { "width": 96,
                     "height": 96,
                     "url": "https://sn3302files..."
                   }
        }
      ]
    }
  ]
}
```

## <a name="size-values"></a><span data-ttu-id="20056-170">サイズの値</span><span class="sxs-lookup"><span data-stu-id="20056-170">Size values</span></span>

<span data-ttu-id="20056-p110">次の表で、使用可能なサムネイルのサイズを定義します。サムネイルの任意のサイズを要求できますが、定義済みの値が存在する可能性が高く、値は即時に返されます。</span><span class="sxs-lookup"><span data-stu-id="20056-p110">This table defines the possible thumbnail sizes. While you can request any arbitrary thumbnail size, the defined values are likely to exist and return a value quickly:</span></span>

| <span data-ttu-id="20056-173">名前</span><span class="sxs-lookup"><span data-stu-id="20056-173">Name</span></span>           | <span data-ttu-id="20056-174">解像度</span><span class="sxs-lookup"><span data-stu-id="20056-174">Resolution</span></span>  | <span data-ttu-id="20056-175">縦横比</span><span class="sxs-lookup"><span data-stu-id="20056-175">Aspect Ratio</span></span> | <span data-ttu-id="20056-176">説明</span><span class="sxs-lookup"><span data-stu-id="20056-176">Description</span></span>                                                          |
|:---------------|:------------|:-------------|:---------------------------------------------------------------------|
| `small`        | <span data-ttu-id="20056-177">96 longest</span><span class="sxs-lookup"><span data-stu-id="20056-177">96 longest</span></span>  | <span data-ttu-id="20056-178">Original</span><span class="sxs-lookup"><span data-stu-id="20056-178">Original</span></span>     | <span data-ttu-id="20056-179">圧縮率の高い小さなサムネイルは、正方形にトリミングされます。</span><span class="sxs-lookup"><span data-stu-id="20056-179">Small, highly compressed thumbnail cropped to a square aspect ratio.</span></span> |
| `medium`       | <span data-ttu-id="20056-180">176 longest</span><span class="sxs-lookup"><span data-stu-id="20056-180">176 longest</span></span> | <span data-ttu-id="20056-181">Original</span><span class="sxs-lookup"><span data-stu-id="20056-181">Original</span></span>     | <span data-ttu-id="20056-182">OneDrive の Web ビューの標準的なアイテムのサイズにトリミングされます。</span><span class="sxs-lookup"><span data-stu-id="20056-182">Cropped to the standard item size for the OneDrive web view.</span></span>         |
| `large`        | <span data-ttu-id="20056-183">800 longest</span><span class="sxs-lookup"><span data-stu-id="20056-183">800 longest</span></span> | <span data-ttu-id="20056-184">Original</span><span class="sxs-lookup"><span data-stu-id="20056-184">Original</span></span>     | <span data-ttu-id="20056-185">サムネイルの長辺が 800 ピクセルになるよう、サイズ変更されます。</span><span class="sxs-lookup"><span data-stu-id="20056-185">Thumbnail with the longest edge resized to 800 pixels.</span></span>               |
| `smallSquare`  | <span data-ttu-id="20056-186">96x96</span><span class="sxs-lookup"><span data-stu-id="20056-186">96x96</span></span>       | <span data-ttu-id="20056-187">正方形にトリミング</span><span class="sxs-lookup"><span data-stu-id="20056-187">Square Crop</span></span>  | <span data-ttu-id="20056-188">小さな正方形のサムネイル</span><span class="sxs-lookup"><span data-stu-id="20056-188">Small square thumbnail</span></span>                                               |
| `mediumSquare` | <span data-ttu-id="20056-189">176x176</span><span class="sxs-lookup"><span data-stu-id="20056-189">176x176</span></span>     | <span data-ttu-id="20056-190">正方形にトリミング</span><span class="sxs-lookup"><span data-stu-id="20056-190">Square Crop</span></span>  | <span data-ttu-id="20056-191">小さな正方形のサムネイル</span><span class="sxs-lookup"><span data-stu-id="20056-191">Small square thumbnail</span></span>                                               |
| `largeSquare`  | <span data-ttu-id="20056-192">800x800</span><span class="sxs-lookup"><span data-stu-id="20056-192">800x800</span></span>     | <span data-ttu-id="20056-193">正方形にトリミング</span><span class="sxs-lookup"><span data-stu-id="20056-193">Square Crop</span></span>  | <span data-ttu-id="20056-194">大きな正方形のサムネイル</span><span class="sxs-lookup"><span data-stu-id="20056-194">Large square thumbnail</span></span>                                               |

## <a name="requesting-custom-thumbnail-sizes"></a><span data-ttu-id="20056-195">カスタムのサムネイル サイズを要求する</span><span class="sxs-lookup"><span data-stu-id="20056-195">Retrieve custom thumbnail sizes</span></span>

<span data-ttu-id="20056-196">定義済みのサイズに加えて、アプリでは、先頭に `c` を付けたサムネイルのディメンション (寸法) を指定することで、カスタムのサムネイル サイズを要求できます。</span><span class="sxs-lookup"><span data-stu-id="20056-196">In addition to the defined sizes, your app can request a custom thumbnail size by specifying the dimensions of the thumbnail prefixed with `c`.</span></span>
<span data-ttu-id="20056-197">たとえば、アプリで 300x400 のサムネイルが必要な場合は、そのサイズを次に示すように要求できます。</span><span class="sxs-lookup"><span data-stu-id="20056-197">For example if you need thumbnails that are 300x400, you can request that size like this:</span></span>

<!-- { "name": "get-thumbnail-custom-size", "scopes": "files.read" } -->

```http
GET /me/drive/items/{item-id}/thumbnails?select=c300x400_Crop
```

<span data-ttu-id="20056-198">これにより、次に示すように選択したカスタムのサムネイル サイズのみの応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="20056-198">Which responds with just the custom thumbnail size selected:</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.thumbnailSet)" } -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "id": "0",
      "c300x400_Crop": { "height": 300, "width": 400, "url": "https://sn3302files.onedrive.com/123"},
    }
  ]
}
```

<span data-ttu-id="20056-199">要求するサムネイルのサイズの後ろに、次に示すオプションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="20056-199">You can specify the following options after the size of the thumbnail requested:</span></span>

### <a name="examples-of-custom-identifiers"></a><span data-ttu-id="20056-200">カスタム識別子の例</span><span class="sxs-lookup"><span data-stu-id="20056-200">Examples of custom identifiers</span></span>

| <span data-ttu-id="20056-201">サムネイル識別子</span><span class="sxs-lookup"><span data-stu-id="20056-201">Thumbnail identifier</span></span> | <span data-ttu-id="20056-202">解像度</span><span class="sxs-lookup"><span data-stu-id="20056-202">Resolution</span></span>             | <span data-ttu-id="20056-203">縦横比</span><span class="sxs-lookup"><span data-stu-id="20056-203">Aspect ratio</span></span> | <span data-ttu-id="20056-204">説明</span><span class="sxs-lookup"><span data-stu-id="20056-204">Description</span></span>                                                                                                                                         |
|:---------------------|:-----------------------|:-------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20056-205">c300x400</span><span class="sxs-lookup"><span data-stu-id="20056-205">c300x400</span></span>             | <span data-ttu-id="20056-206">300x400 のボックスに制限されます</span><span class="sxs-lookup"><span data-stu-id="20056-206">Bounded by 300x400 box</span></span> | <span data-ttu-id="20056-207">Original</span><span class="sxs-lookup"><span data-stu-id="20056-207">Original</span></span>     | <span data-ttu-id="20056-208">300x400 ピクセルのボックスに収まるサムネイルを生成します。縦横比は維持されます。</span><span class="sxs-lookup"><span data-stu-id="20056-208">Generate a thumbnail that fits inside a 300x400 pixel box, maintaining aspect ratio</span></span>                                                                 |
| <span data-ttu-id="20056-209">c300x400_Crop</span><span class="sxs-lookup"><span data-stu-id="20056-209">c300x400_Crop</span></span>        | <span data-ttu-id="20056-210">300x400</span><span class="sxs-lookup"><span data-stu-id="20056-210">300x400</span></span>                | <span data-ttu-id="20056-211">トリミング</span><span class="sxs-lookup"><span data-stu-id="20056-211">Cropped</span></span>      | <span data-ttu-id="20056-212">300x400 ピクセルのサムネイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="20056-212">Generate a thumbnail that is 300x400 pixels.</span></span> <span data-ttu-id="20056-213">これは、300x400 のボックスに収まるように画像のサイズを変更し、このボックスに収まらない部分をトリミングするように動作します。</span><span class="sxs-lookup"><span data-stu-id="20056-213">This works by resizing the image to fill the 300x400 box and cropping whatever spills outside the box.</span></span> |

<span data-ttu-id="20056-214">**注:** 返されるサムネイルのピクセル ディメンションは要求されたものと正確に一致しないことがありますが、縦横比は一致します。</span><span class="sxs-lookup"><span data-stu-id="20056-214">**Note:** The thumbnail returned may not exactly match the pixel dimensions that was requested, but will match the aspect ratio.</span></span>
<span data-ttu-id="20056-215">サムネイルがすでに存在しており、要求された解像度に簡単に拡大縮小できる場合、要求されたものよりも大きいサムネイルが返されることがあります。</span><span class="sxs-lookup"><span data-stu-id="20056-215">In some cases, a larger thumbnail may be returned than was requested, if the thumbnail already exists and can easily be scaled to match the requested resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="20056-216">備考</span><span class="sxs-lookup"><span data-stu-id="20056-216">Remarks</span></span>

<span data-ttu-id="20056-217">**注:** OneDrive for Business および SharePoint の場合:</span><span class="sxs-lookup"><span data-stu-id="20056-217">**Note** In OneDrive for Business and SharePoint:</span></span>

<span data-ttu-id="20056-218">次の呼び出しを使用したサムネイル コレクションの展開は機能しません。</span><span class="sxs-lookup"><span data-stu-id="20056-218">Using these calls to expand the thumbnails collection will not work:</span></span>

* `GET /drive/root:/{item-path}?expand=children(expand=thumbnails)`
* `GET /drive/items/{item-id}/children?expand=thumbnails`

<span data-ttu-id="20056-219">サムネイルは、SharePoint Server 2016 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="20056-219">Thumbnails are not supported on SharePoint Server 2016.</span></span>

### <a name="error-responses"></a><span data-ttu-id="20056-220">エラー応答</span><span class="sxs-lookup"><span data-stu-id="20056-220">Error responses</span></span>

<span data-ttu-id="20056-221">エラーがどのように返されるかについては、「[エラー応答][error-response]」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20056-221">See [Error Responses][error-response] for more info about how errors are returned.</span></span>

[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "Get metadata and content for thumbnails of multiple sizes for OneDrive items.",
  "keywords": "thumbnail,content,download,sizes",
  "section": "documentation",
  "tocPath": "Items/Thumbnails"
} -->