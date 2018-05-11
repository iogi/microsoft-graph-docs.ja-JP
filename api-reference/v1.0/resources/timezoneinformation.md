# <a name="timezoneinformation-resource-type"></a><span data-ttu-id="db3cd-101">timeZoneInformation リソースの種類</span><span class="sxs-lookup"><span data-stu-id="db3cd-101">timeZoneInformation resource type</span></span>


<span data-ttu-id="db3cd-102">タイム ゾーンを表します。</span><span class="sxs-lookup"><span data-stu-id="db3cd-102">Represents information about a time zone.</span></span> <span data-ttu-id="db3cd-103">サポートされる形式は、Windows 形式です。現在既知の問題が解決されている場合は、[Internet Assigned Numbers Authority (IANA) タイム ゾーン](http://www.iana.org/time-zones) (Olson タイム ゾーンとも呼ばれる) 形式もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="db3cd-103">The supported format is Windows, and [Internet Assigned Numbers Authority (IANA) time zone](http://www.iana.org/time-zones) (also known as Olson time zone) format as well when the current known problem is fixed.</span></span>

## <a name="properties"></a><span data-ttu-id="db3cd-104">プロパティ</span><span class="sxs-lookup"><span data-stu-id="db3cd-104">Properties</span></span>
| <span data-ttu-id="db3cd-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="db3cd-105">Property</span></span>     | <span data-ttu-id="db3cd-106">型</span><span class="sxs-lookup"><span data-stu-id="db3cd-106">Type</span></span>   |<span data-ttu-id="db3cd-107">説明</span><span class="sxs-lookup"><span data-stu-id="db3cd-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="db3cd-108">alias</span><span class="sxs-lookup"><span data-stu-id="db3cd-108">alias</span></span>|<span data-ttu-id="db3cd-109">string</span><span class="sxs-lookup"><span data-stu-id="db3cd-109">string</span></span>|<span data-ttu-id="db3cd-110">タイム ゾーンの識別子。</span><span class="sxs-lookup"><span data-stu-id="db3cd-110">An identifier for the time zone.</span></span>|
|<span data-ttu-id="db3cd-111">displayName</span><span class="sxs-lookup"><span data-stu-id="db3cd-111">displayName</span></span>|<span data-ttu-id="db3cd-112">string</span><span class="sxs-lookup"><span data-stu-id="db3cd-112">string</span></span>|<span data-ttu-id="db3cd-113">タイム ゾーンを表す表示文字列。</span><span class="sxs-lookup"><span data-stu-id="db3cd-113">A display string that represents the time zone.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="db3cd-114">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="db3cd-114">JSON representation</span></span>

<span data-ttu-id="db3cd-115">以下は、リソースの JSON 表記です。</span><span class="sxs-lookup"><span data-stu-id="db3cd-115">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneInformation"
}-->

```json
{
  "alias": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->