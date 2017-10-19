---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CalculatedColumn
ms.openlocfilehash: 44700ba7606243002798ec0ec84c3be30d38ef1f
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2017
---
# <a name="calculatedcolumn-resource-type"></a><span data-ttu-id="83da7-102">CalculatedColumn リソースの種類</span><span class="sxs-lookup"><span data-stu-id="83da7-102">CalculatedColumn resource type</span></span>

<span data-ttu-id="83da7-103">[columnDefinition](columnDefinition.md) リソースの **calculatedColumn** は、列のデータがサイト内の他の列に基づいて計算されることを示します。</span><span class="sxs-lookup"><span data-stu-id="83da7-103">The **calculatedColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's data is calculated based on other columns in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="83da7-104">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="83da7-104">JSON representation</span></span>

<span data-ttu-id="83da7-105">以下は、**calculatedColumn** リソースの JSON 表記です。</span><span class="sxs-lookup"><span data-stu-id="83da7-105">Here is a JSON representation of a **driveItem** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.calculatedColumn" } -->

```json
{
  "format": "dateOnly | dateTime",
  "formula": "=[Column1]+[Column2]+[Column3]",
  "outputType": "boolean | currency | dateTime | number | text",
}
```

## <a name="properties"></a><span data-ttu-id="83da7-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="83da7-106">Properties</span></span>

| <span data-ttu-id="83da7-107">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="83da7-107">Property name</span></span>  | <span data-ttu-id="83da7-108">種類</span><span class="sxs-lookup"><span data-stu-id="83da7-108">Type</span></span>    | <span data-ttu-id="83da7-109">説明</span><span class="sxs-lookup"><span data-stu-id="83da7-109">Description</span></span>
|:---------------|:--------|:--------------------------------------------------
| <span data-ttu-id="83da7-110">**format**</span><span class="sxs-lookup"><span data-stu-id="83da7-110">**format**</span></span>     | <span data-ttu-id="83da7-111">string</span><span class="sxs-lookup"><span data-stu-id="83da7-111">string</span></span>  | <span data-ttu-id="83da7-112">`dateTime` 出力の種類に対する値の形式。</span><span class="sxs-lookup"><span data-stu-id="83da7-112">For `dateTime` output types, the format of the value.</span></span> <span data-ttu-id="83da7-113">`dateOnly` または `dateTime` のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="83da7-113">Must be one of `dateOnly` or `dateTime`.</span></span>
| <span data-ttu-id="83da7-114">**formula**</span><span class="sxs-lookup"><span data-stu-id="83da7-114">**formula**</span></span>    | <span data-ttu-id="83da7-115">string</span><span class="sxs-lookup"><span data-stu-id="83da7-115">string</span></span>  | <span data-ttu-id="83da7-116">この列の値を計算するために使用する数式。</span><span class="sxs-lookup"><span data-stu-id="83da7-116">The formula used to compute the value for this column.</span></span>
| <span data-ttu-id="83da7-117">**outputType**</span><span class="sxs-lookup"><span data-stu-id="83da7-117">**outputType**</span></span> | <span data-ttu-id="83da7-118">string</span><span class="sxs-lookup"><span data-stu-id="83da7-118">string</span></span>  | <span data-ttu-id="83da7-119">この列の値の形式を設定するために使用する出力の種類。</span><span class="sxs-lookup"><span data-stu-id="83da7-119">The output type used to format values in this column.</span></span> <span data-ttu-id="83da7-120">`boolean`、`currency`、`dateTime`、`number`、`text` のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="83da7-120">Must be one of `boolean`, `currency`, `dateTime`, `number`, or `text`.</span></span>

<span data-ttu-id="83da7-121">SharePoint の数式は、Excel の数式のような構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="83da7-121">SharePoint formulas use a syntax similar to Excel formulas.</span></span>
<span data-ttu-id="83da7-122">詳細については、「[SharePoint リストの一般的な数式の例][SPFormulas]」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83da7-122">See [Examples of common formulas in SharePoint Lists][SPFormulas] for more information.</span></span>

[SPFormulas]: https://support.office.com/en-us/article/Examples-of-common-formulas-in-SharePoint-Lists-d81f5f21-2b4e-45ce-b170-bf7ebf6988b3

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CalculatedColumn"
} -->