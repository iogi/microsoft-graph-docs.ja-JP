# <a name="reportroot-getteamsdeviceusagedistributionusercounts"></a><span data-ttu-id="04995-101">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span><span class="sxs-lookup"><span data-stu-id="04995-101">reportRoot: getTeamsDeviceUsageDistributionUserCounts</span></span>

<span data-ttu-id="04995-102">デバイスの種類ごとに、選択した期間の Microsoft Teams のユニーク ユーザーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="04995-102">Get the number of Microsoft Teams unique users by device type over the selected time period.</span></span>

## <a name="permissions"></a><span data-ttu-id="04995-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="04995-103">Permissions</span></span>

<span data-ttu-id="04995-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04995-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="04995-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="04995-106">Permission type</span></span>                        | <span data-ttu-id="04995-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="04995-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="04995-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="04995-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="04995-109">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="04995-109">Not supported.</span></span>                           |
| <span data-ttu-id="04995-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="04995-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="04995-111">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="04995-111">Not supported.</span></span>                           |
| <span data-ttu-id="04995-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="04995-112">Application</span></span>                            | <span data-ttu-id="04995-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="04995-113">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="04995-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="04995-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsDeviceUsageDistributionUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="04995-115">要求パラメーター</span><span class="sxs-lookup"><span data-stu-id="04995-115">Request parameters</span></span>

<span data-ttu-id="04995-116">要求 URL に、次のパラメーターと有効な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="04995-116">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="04995-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04995-117">Parameter</span></span> | <span data-ttu-id="04995-118">型</span><span class="sxs-lookup"><span data-stu-id="04995-118">Type</span></span>   | <span data-ttu-id="04995-119">説明</span><span class="sxs-lookup"><span data-stu-id="04995-119">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="04995-120">period</span><span class="sxs-lookup"><span data-stu-id="04995-120">period</span></span>    | <span data-ttu-id="04995-121">文字列</span><span class="sxs-lookup"><span data-stu-id="04995-121">string</span></span> | <span data-ttu-id="04995-122">レポートを集計する期間の長さを指定します。</span><span class="sxs-lookup"><span data-stu-id="04995-122">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="04995-123">{period_value} でサポートされている値は D7、D30、D90、D180 です。</span><span class="sxs-lookup"><span data-stu-id="04995-123">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="04995-124">これらの値は、D*n* の形式 (*n* はレポートを集計する日数) に従います。</span><span class="sxs-lookup"><span data-stu-id="04995-124">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="04995-125">必須。</span><span class="sxs-lookup"><span data-stu-id="04995-125">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="04995-126">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="04995-126">Request headers</span></span>

| <span data-ttu-id="04995-127">名前</span><span class="sxs-lookup"><span data-stu-id="04995-127">Name</span></span>          | <span data-ttu-id="04995-128">説明</span><span class="sxs-lookup"><span data-stu-id="04995-128">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="04995-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="04995-129">Authorization</span></span> | <span data-ttu-id="04995-p103">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="04995-p103">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="04995-132">応答</span><span class="sxs-lookup"><span data-stu-id="04995-132">Response</span></span>

<span data-ttu-id="04995-133">成功すると、レポートの事前認証されたダウンロード URL にリダイレクトする `302 Found` 応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="04995-133">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="04995-134">その URL は、応答の `Location` ヘッダー内にあります。</span><span class="sxs-lookup"><span data-stu-id="04995-134">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="04995-135">事前認証されたダウンロード URL は、短期間 (数分) のみ有効で、`Authorization` ヘッダーを必要としません。</span><span class="sxs-lookup"><span data-stu-id="04995-135">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="04995-136">この CSV ファイルには、次の列ヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="04995-136">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="04995-137">レポートの更新日</span><span class="sxs-lookup"><span data-stu-id="04995-137">Report Refresh Date</span></span>
- <span data-ttu-id="04995-138">Web</span><span class="sxs-lookup"><span data-stu-id="04995-138">Web</span></span>
- <span data-ttu-id="04995-139">Windows スマートフォン</span><span class="sxs-lookup"><span data-stu-id="04995-139">Windows Phone</span></span>
- <span data-ttu-id="04995-140">Android スマートフォン</span><span class="sxs-lookup"><span data-stu-id="04995-140">Android Phone</span></span>
- <span data-ttu-id="04995-141">iOS</span><span class="sxs-lookup"><span data-stu-id="04995-141">iOS</span></span>
- <span data-ttu-id="04995-142">Mac</span><span class="sxs-lookup"><span data-stu-id="04995-142">Mac</span></span>
- <span data-ttu-id="04995-143">Windows</span><span class="sxs-lookup"><span data-stu-id="04995-143">Windows</span></span>
- <span data-ttu-id="04995-144">レポート期間</span><span class="sxs-lookup"><span data-stu-id="04995-144">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="04995-145">例</span><span class="sxs-lookup"><span data-stu-id="04995-145">Example</span></span>

#### <a name="request"></a><span data-ttu-id="04995-146">要求</span><span class="sxs-lookup"><span data-stu-id="04995-146">Request</span></span>

<span data-ttu-id="04995-147">要求の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="04995-147">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsdeviceusagedistributionusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsDeviceUsageDistributionUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="04995-148">応答</span><span class="sxs-lookup"><span data-stu-id="04995-148">Response</span></span>

<span data-ttu-id="04995-149">応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="04995-149">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="04995-150">302 リダイレクトに従うと、ダウンロードされる CSV ファイルは次のスキーマを持つことになります。</span><span class="sxs-lookup"><span data-stu-id="04995-150">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Web,Windows Phone,Android Phone,iOS,Mac,Windows,Report Period
```