# <a name="reportroot-getteamsuseractivityuserdetail"></a><span data-ttu-id="43e59-101">reportRoot: getTeamsUserActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="43e59-101">reportRoot: getTeamsUserActivityUserDetail</span></span>

<span data-ttu-id="43e59-102">ユーザーごとに、Microsoft Teams ユーザー アクティビティの詳細を取得します。</span><span class="sxs-lookup"><span data-stu-id="43e59-102">Get details about Microsoft Teams user activity by user.</span></span>

## <a name="permissions"></a><span data-ttu-id="43e59-103">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="43e59-103">Permissions</span></span>

<span data-ttu-id="43e59-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="43e59-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="43e59-106">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="43e59-106">Permission type</span></span>                        | <span data-ttu-id="43e59-107">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="43e59-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="43e59-108">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="43e59-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="43e59-109">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="43e59-109">Not supported.</span></span>                           |
| <span data-ttu-id="43e59-110">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="43e59-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="43e59-111">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="43e59-111">Not supported.</span></span>                           |
| <span data-ttu-id="43e59-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="43e59-112">Application</span></span>                            | <span data-ttu-id="43e59-113">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="43e59-113">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="43e59-114">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="43e59-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserDetail(period='{period_value}')
GET /reports/getTeamsUserActivityUserDetail(date={date_value})
```

## <a name="request-parameters"></a><span data-ttu-id="43e59-115">要求パラメーター</span><span class="sxs-lookup"><span data-stu-id="43e59-115">Request parameters</span></span>

<span data-ttu-id="43e59-116">要求 URL に、次のうちの 1 つのパラメーターと有効な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="43e59-116">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="43e59-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43e59-117">Parameter</span></span> | <span data-ttu-id="43e59-118">型</span><span class="sxs-lookup"><span data-stu-id="43e59-118">Type</span></span>   | <span data-ttu-id="43e59-119">説明</span><span class="sxs-lookup"><span data-stu-id="43e59-119">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="43e59-120">period</span><span class="sxs-lookup"><span data-stu-id="43e59-120">period</span></span>    | <span data-ttu-id="43e59-121">文字列</span><span class="sxs-lookup"><span data-stu-id="43e59-121">string</span></span> | <span data-ttu-id="43e59-122">レポートを集計する期間の長さを指定します。</span><span class="sxs-lookup"><span data-stu-id="43e59-122">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="43e59-123">{period_value} でサポートされている値は D7、D30、D90、D180 です。</span><span class="sxs-lookup"><span data-stu-id="43e59-123">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="43e59-124">これらの値は、D*n* の形式 (*n* はレポートを集計する日数) に従います。</span><span class="sxs-lookup"><span data-stu-id="43e59-124">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> |
| <span data-ttu-id="43e59-125">date</span><span class="sxs-lookup"><span data-stu-id="43e59-125">date</span></span>      | <span data-ttu-id="43e59-126">日付</span><span class="sxs-lookup"><span data-stu-id="43e59-126">Date</span></span>   | <span data-ttu-id="43e59-127">何らかのアクティビティを実行したユーザーを表示する日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="43e59-127">Specifies the date for which you would like to view the users who performed any activity.</span></span> <span data-ttu-id="43e59-128">{date_value} は YYYY-MM-DD の形式にします。</span><span class="sxs-lookup"><span data-stu-id="43e59-128">{date_value} must have a format of YYYY-MM-DD.</span></span> <span data-ttu-id="43e59-129">このレポートは、過去 30 日間のみ利用可能であり、{date_value} はその範囲内の日付である必要があります。</span><span class="sxs-lookup"><span data-stu-id="43e59-129">As this report is only available for the past 30 days, {date_value} should be a date from that range.</span></span> |

> <span data-ttu-id="43e59-130">**注:** URL に期間または日付を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43e59-130">**Note:** You need to set either period or date in the URL.</span></span>

## <a name="request-headers"></a><span data-ttu-id="43e59-131">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="43e59-131">Request headers</span></span>

| <span data-ttu-id="43e59-132">名前</span><span class="sxs-lookup"><span data-stu-id="43e59-132">Name</span></span>          | <span data-ttu-id="43e59-133">説明</span><span class="sxs-lookup"><span data-stu-id="43e59-133">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="43e59-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="43e59-134">Authorization</span></span> | <span data-ttu-id="43e59-p104">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="43e59-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="43e59-137">応答</span><span class="sxs-lookup"><span data-stu-id="43e59-137">Response</span></span>

<span data-ttu-id="43e59-138">成功すると、レポートの事前認証されたダウンロード URL にリダイレクトする `302 Found` 応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="43e59-138">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="43e59-139">その URL は、応答の `Location` ヘッダー内にあります。</span><span class="sxs-lookup"><span data-stu-id="43e59-139">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="43e59-140">事前認証されたダウンロード URL は、短期間 (数分) のみ有効で、`Authorization` ヘッダーを必要としません。</span><span class="sxs-lookup"><span data-stu-id="43e59-140">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="43e59-141">この CSV ファイルには、次の列ヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="43e59-141">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="43e59-142">レポートの更新日</span><span class="sxs-lookup"><span data-stu-id="43e59-142">Report Refresh Date</span></span>
- <span data-ttu-id="43e59-143">ユーザー プリンシパル名</span><span class="sxs-lookup"><span data-stu-id="43e59-143">User Principal Name</span></span>
- <span data-ttu-id="43e59-144">最後のアクティビティ日付</span><span class="sxs-lookup"><span data-stu-id="43e59-144">Last Activity Date</span></span>
- <span data-ttu-id="43e59-145">削除済み</span><span class="sxs-lookup"><span data-stu-id="43e59-145">Is Deleted</span></span>
- <span data-ttu-id="43e59-146">削除日</span><span class="sxs-lookup"><span data-stu-id="43e59-146">Deleted Date</span></span>
- <span data-ttu-id="43e59-147">割り当て済み製品</span><span class="sxs-lookup"><span data-stu-id="43e59-147">Assigned Products</span></span>
- <span data-ttu-id="43e59-148">チーム チャット メッセージ数</span><span class="sxs-lookup"><span data-stu-id="43e59-148">Team Chat Message Count</span></span>
- <span data-ttu-id="43e59-149">非公開チャット メッセージ数</span><span class="sxs-lookup"><span data-stu-id="43e59-149">Private Chat Message Count</span></span>
- <span data-ttu-id="43e59-150">通話数</span><span class="sxs-lookup"><span data-stu-id="43e59-150">Call Count</span></span>
- <span data-ttu-id="43e59-151">会議数</span><span class="sxs-lookup"><span data-stu-id="43e59-151">Meeting Count</span></span>
- <span data-ttu-id="43e59-152">その他のアクションの有無</span><span class="sxs-lookup"><span data-stu-id="43e59-152">Has Other Action</span></span>
- <span data-ttu-id="43e59-153">レポート期間</span><span class="sxs-lookup"><span data-stu-id="43e59-153">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="43e59-154">例</span><span class="sxs-lookup"><span data-stu-id="43e59-154">Example</span></span>

#### <a name="request"></a><span data-ttu-id="43e59-155">要求</span><span class="sxs-lookup"><span data-stu-id="43e59-155">Request</span></span>

<span data-ttu-id="43e59-156">要求の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="43e59-156">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityuserdetail"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserDetail(period='D7')
```

#### <a name="response"></a><span data-ttu-id="43e59-157">応答</span><span class="sxs-lookup"><span data-stu-id="43e59-157">Response</span></span>

<span data-ttu-id="43e59-158">応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="43e59-158">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="43e59-159">302 リダイレクトに従うと、ダウンロードされる CSV ファイルは次のスキーマを持つことになります。</span><span class="sxs-lookup"><span data-stu-id="43e59-159">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,User Principal Name,Last Activity Date,Is Deleted,Deleted Date,Assigned Products,Team Chat Message Count,Private Chat Message Count,Call Count,Meeting Count,Has Other Action,Report Period
```