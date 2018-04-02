# <a name="reportroot-getteamsuseractivityusercounts"></a><span data-ttu-id="5540b-101">reportRoot: getTeamsUserActivityUserCounts</span><span class="sxs-lookup"><span data-stu-id="5540b-101">reportRoot: getTeamsUserActivityUserCounts</span></span>

<span data-ttu-id="5540b-102">アクティビティの種類ごとに、Microsoft Teams ユーザーの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="5540b-102">Get the number of Microsoft Teams users by activity type.</span></span> <span data-ttu-id="5540b-103">アクティビティの種類は、チーム チャット メッセージ、非公開チャット メッセージ、通話、または会議の数です。</span><span class="sxs-lookup"><span data-stu-id="5540b-103">The activity types are number of teams chat messages, private chat messages, calls, or meetings.</span></span>

## <a name="permissions"></a><span data-ttu-id="5540b-104">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="5540b-104">Permissions</span></span>

<span data-ttu-id="5540b-p102">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5540b-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="5540b-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="5540b-107">Permission type</span></span>                        | <span data-ttu-id="5540b-108">アクセス許可 (特権の小さいものから大きいものへ)</span><span class="sxs-lookup"><span data-stu-id="5540b-108">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :--------------------------------------- |
| <span data-ttu-id="5540b-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="5540b-109">Delegated (work or school account)</span></span>     | <span data-ttu-id="5540b-110">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5540b-110">Not supported.</span></span>                           |
| <span data-ttu-id="5540b-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="5540b-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5540b-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5540b-112">Not supported.</span></span>                           |
| <span data-ttu-id="5540b-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5540b-113">Application</span></span>                            | <span data-ttu-id="5540b-114">Reports.Read.All</span><span class="sxs-lookup"><span data-stu-id="5540b-114">Reports.Read.All</span></span>                         |

## <a name="http-request"></a><span data-ttu-id="5540b-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="5540b-115">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
GET /reports/getTeamsUserActivityUserCounts(period='{period_value}')
```

## <a name="request-parameters"></a><span data-ttu-id="5540b-116">要求パラメーター</span><span class="sxs-lookup"><span data-stu-id="5540b-116">Request parameters</span></span>

<span data-ttu-id="5540b-117">要求 URL に、次のパラメーターと有効な値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5540b-117">In the request URL, provide the following query parameter with a valid value.</span></span>

| <span data-ttu-id="5540b-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5540b-118">Parameter</span></span> | <span data-ttu-id="5540b-119">型</span><span class="sxs-lookup"><span data-stu-id="5540b-119">Type</span></span>   | <span data-ttu-id="5540b-120">説明</span><span class="sxs-lookup"><span data-stu-id="5540b-120">Description</span></span>                              |
| :-------- | :----- | :--------------------------------------- |
| <span data-ttu-id="5540b-121">period</span><span class="sxs-lookup"><span data-stu-id="5540b-121">period</span></span>    | <span data-ttu-id="5540b-122">文字列</span><span class="sxs-lookup"><span data-stu-id="5540b-122">string</span></span> | <span data-ttu-id="5540b-123">レポートを集計する期間の長さを指定します。</span><span class="sxs-lookup"><span data-stu-id="5540b-123">Specifies the length of time over which the report is aggregated.</span></span> <span data-ttu-id="5540b-124">{period_value} でサポートされている値は D7、D30、D90、D180 です。</span><span class="sxs-lookup"><span data-stu-id="5540b-124">The supported values for {period_value} are: D7, D30, D90, and D180.</span></span> <span data-ttu-id="5540b-125">これらの値は、D*n* の形式 (*n* はレポートを集計する日数) に従います。</span><span class="sxs-lookup"><span data-stu-id="5540b-125">These values follow the format D*n* where *n* represents the number of days over which the report is aggregated.</span></span> <span data-ttu-id="5540b-126">必須。</span><span class="sxs-lookup"><span data-stu-id="5540b-126">Required.</span></span> |

## <a name="request-headers"></a><span data-ttu-id="5540b-127">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="5540b-127">Request headers</span></span>

| <span data-ttu-id="5540b-128">名前</span><span class="sxs-lookup"><span data-stu-id="5540b-128">Name</span></span>          | <span data-ttu-id="5540b-129">説明</span><span class="sxs-lookup"><span data-stu-id="5540b-129">Description</span></span>               |
| :------------ | :------------------------ |
| <span data-ttu-id="5540b-130">Authorization</span><span class="sxs-lookup"><span data-stu-id="5540b-130">Authorization</span></span> | <span data-ttu-id="5540b-p104">ベアラー {トークン}。必須。</span><span class="sxs-lookup"><span data-stu-id="5540b-p104">Bearer {token}. Required.</span></span> |

## <a name="response"></a><span data-ttu-id="5540b-133">応答</span><span class="sxs-lookup"><span data-stu-id="5540b-133">Response</span></span>

<span data-ttu-id="5540b-134">成功すると、レポートの事前認証されたダウンロード URL にリダイレクトする `302 Found` 応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="5540b-134">If successful, this method returns a `302 Found` response that redirects to a preauthenticated download URL for the report.</span></span> <span data-ttu-id="5540b-135">その URL は、応答の `Location` ヘッダー内にあります。</span><span class="sxs-lookup"><span data-stu-id="5540b-135">That URL can be found in the `Location` header in the response.</span></span>

<span data-ttu-id="5540b-136">事前認証されたダウンロード URL は、短期間 (数分) のみ有効で、`Authorization` ヘッダーを必要としません。</span><span class="sxs-lookup"><span data-stu-id="5540b-136">Preauthenticated download URLs are only valid for a short period of time (a few minutes) and do not require an `Authorization` header.</span></span>

<span data-ttu-id="5540b-137">この CSV ファイルには、次の列ヘッダーがあります。</span><span class="sxs-lookup"><span data-stu-id="5540b-137">The CSV file has the following headers for columns.</span></span>

- <span data-ttu-id="5540b-138">レポートの更新日</span><span class="sxs-lookup"><span data-stu-id="5540b-138">Report Refresh Date</span></span>
- <span data-ttu-id="5540b-139">レポート日付</span><span class="sxs-lookup"><span data-stu-id="5540b-139">Report Date</span></span>
- <span data-ttu-id="5540b-140">チーム チャット メッセージ</span><span class="sxs-lookup"><span data-stu-id="5540b-140">Team Chat Messages</span></span>
- <span data-ttu-id="5540b-141">非公開チャット メッセージ</span><span class="sxs-lookup"><span data-stu-id="5540b-141">Private Chat Messages</span></span>
- <span data-ttu-id="5540b-142">通話</span><span class="sxs-lookup"><span data-stu-id="5540b-142">API Calls</span></span>
- <span data-ttu-id="5540b-143">会議</span><span class="sxs-lookup"><span data-stu-id="5540b-143">meetings</span></span>
- <span data-ttu-id="5540b-144">その他のアクション</span><span class="sxs-lookup"><span data-stu-id="5540b-144">Other Actions</span></span>
- <span data-ttu-id="5540b-145">レポート期間</span><span class="sxs-lookup"><span data-stu-id="5540b-145">Report Period</span></span>

## <a name="example"></a><span data-ttu-id="5540b-146">例</span><span class="sxs-lookup"><span data-stu-id="5540b-146">Example</span></span>

#### <a name="request"></a><span data-ttu-id="5540b-147">要求</span><span class="sxs-lookup"><span data-stu-id="5540b-147">Request</span></span>

<span data-ttu-id="5540b-148">要求の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5540b-148">The following is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "reportroot_getteamsuseractivityusercounts"
}-->

```http
GET https://graph.microsoft.com/v1.0/reports/getTeamsUserActivityUserCounts(period='D7')
```

#### <a name="response"></a><span data-ttu-id="5540b-149">応答</span><span class="sxs-lookup"><span data-stu-id="5540b-149">Response</span></span>

<span data-ttu-id="5540b-150">応答の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5540b-150">The following is an example of the response.</span></span>

<!-- { "blockType": "ignored" } --> 

```http
HTTP/1.1 302 Found
Content-Type: text/plain
Location: https://reports.office.com/data/download/JDFKdf2_eJXKS034dbc7e0t__XDe
```

<span data-ttu-id="5540b-151">302 リダイレクトに従うと、ダウンロードされる CSV ファイルは次のスキーマを持つことになります。</span><span class="sxs-lookup"><span data-stu-id="5540b-151">Follow the 302 redirection and the CSV file that downloads will have the following schema.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "stream"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

Report Refresh Date,Report Date,Team Chat Messages,Private Chat Messages,Calls,Meetings,Other Actions,Report Period
```