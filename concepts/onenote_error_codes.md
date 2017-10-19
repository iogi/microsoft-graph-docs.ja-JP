# <a name="error-codes-for-onenote-apis-in-microsoft-graph"></a><span data-ttu-id="03d32-101">Microsoft Graph の OneNote API のエラー コード</span><span class="sxs-lookup"><span data-stu-id="03d32-101">Error codes for OneNote APIs in Microsoft Graph</span></span>

<span data-ttu-id="03d32-102">この記事では、API を通して送信した要求が失敗した場合に、Microsoft Graph の OneNote API から返されるエラー コードについて説明します。</span><span class="sxs-lookup"><span data-stu-id="03d32-102">This article describes error and warning codes that are returned by the OneNote API whenever a request sent through the API fails.</span></span>

## <a name="error-response-example"></a><span data-ttu-id="03d32-103">エラー応答例</span><span class="sxs-lookup"><span data-stu-id="03d32-103">Error response example</span></span>
<span data-ttu-id="03d32-p101">送信した要求でエラーが発生すると、OneNote API はその要求の実行を停止し、エラー応答を JSON オブジェクトとして返します。エラー応答には、関連付けられているエラー コード、メッセージ、およびこの記事の該当するセクションへのリンクが含まれます。次の例は、エラー応答の様子を示しています。</span><span class="sxs-lookup"><span data-stu-id="03d32-p101">When your request generates an error, the OneNote API stops performing the request and returns an error response as a JSON object. An error response contains the associated error code, a message, and a link to the appropriate section of this article. The following example shows how an error response looks.</span></span>

```json
{
   "error":{
      "code":"10002",
      "message":"The service is currently unavailable. Please try again later.",
      "innerError": {
        "requestId": "request-id",
        "date": "date-time"
      }
   }
}
```

<span data-ttu-id="03d32-107">Microsoft Graph エラーの詳細については、「[Microsoft Graph エラー応答およびリソースの種類](errors.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-107">For more information about Microsoft Graph errors, see [Microsoft Graph error responses and resource types](errors.md).</span></span>

## <a name="codes-from-10001-to-19999"></a><span data-ttu-id="03d32-108">10001 から 19999 のコード</span><span class="sxs-lookup"><span data-stu-id="03d32-108">Codes from 10001 to 19999</span></span>
<span data-ttu-id="03d32-109">サービスで問題が発生したか、サービスからアプリケーションに情報が送られました。</span><span class="sxs-lookup"><span data-stu-id="03d32-109">The service is having problems or is sending information to the application.</span></span>

### <a name="10001"></a><span data-ttu-id="03d32-110">10001</span><span class="sxs-lookup"><span data-stu-id="03d32-110">10001</span></span>
<span data-ttu-id="03d32-111">予期しないエラーが発生し、要求が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="03d32-111">An unexpected error occurred and the request failed.</span></span>

### <a name="10002"></a><span data-ttu-id="03d32-112">10002</span><span class="sxs-lookup"><span data-stu-id="03d32-112">10002</span></span>
<span data-ttu-id="03d32-113">サービスは現在利用できません。</span><span class="sxs-lookup"><span data-stu-id="03d32-113">The service is not currently available.</span></span>

### <a name="10003"></a><span data-ttu-id="03d32-114">10003</span><span class="sxs-lookup"><span data-stu-id="03d32-114">10003</span></span>
<span data-ttu-id="03d32-p102">現在のユーザーのアカウントで、アクティブな要求の最大数を超えました。アプリは要求を繰り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d32-p102">The current user's account has exceeded the maximum number of active requests. Your app will have to repeat the request.</span></span>

### <a name="10004"></a><span data-ttu-id="03d32-117">10004</span><span class="sxs-lookup"><span data-stu-id="03d32-117">10004</span></span>
<span data-ttu-id="03d32-118">サービスは要求されたセクション内にページを作成できません。そのセクションはパスワードで保護されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-118">The service can't create a page in the requested section because that section is protected by a password.</span></span>

### <a name="10005"></a><span data-ttu-id="03d32-119">10005</span><span class="sxs-lookup"><span data-stu-id="03d32-119">10005</span></span>
<span data-ttu-id="03d32-120">要求内で、**data-render-src** 属性に PDF が含まれる画像タグが最大数を超えました。</span><span class="sxs-lookup"><span data-stu-id="03d32-120">The request contains more than the maximum number of image tags in which the **data-render-src** attribute contains a PDF. See  for more information.</span></span> <span data-ttu-id="03d32-121">「[画像とファイルを追加する](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-images-files)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-121">Add images and files</span></span>

### <a name="10006"></a><span data-ttu-id="03d32-122">10006</span><span class="sxs-lookup"><span data-stu-id="03d32-122">10006</span></span>
<span data-ttu-id="03d32-123">OneNote API は、指定されたセクション内にページを作成できませんでした。そのセクションは破損しています。</span><span class="sxs-lookup"><span data-stu-id="03d32-123">The OneNote API was unable to create a page in the specified section because that section is corrupt.</span></span>

### <a name="10007"></a><span data-ttu-id="03d32-124">10007</span><span class="sxs-lookup"><span data-stu-id="03d32-124">10007</span></span>
<span data-ttu-id="03d32-p104">現在、サーバーがビジー状態であるため、受信した要求を処理できません。後でもう一度やり直してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-p104">The server is too busy to handle the incoming request at this moment. Please try again later.</span></span>

### <a name="10008"></a><span data-ttu-id="03d32-127">10008</span><span class="sxs-lookup"><span data-stu-id="03d32-127">10008</span></span>
<span data-ttu-id="03d32-128">ユーザーまたはグループの OneDrive にある 1 つ以上のドキュメント ライブラリに 5000 を超える OneNote のアイテム (ノートブック、セクション、セクション グループ) が含まれており、API を使用してクエリを実行することができません。</span><span class="sxs-lookup"><span data-stu-id="03d32-128">One or more of the document libraries on the user or group's OneDrive contains more than 5000 OneNote items (notebooks, sections, section groups), and cannot be queried using the API.</span></span> <span data-ttu-id="03d32-129">ユーザーまたはグループのどのドキュメント ライブラリについても、その中の OneNote アイテム数が 5000 を超えることがないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="03d32-129">Please make sure that none of the user or group's document libraries contains more than 5000 OneNote items.</span></span> <span data-ttu-id="03d32-130">軽減の手順については「[OneNote 開発者ブログ](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-130">See the [OneNote Dev blog](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) for mitigation steps.</span></span>

### <a name="10012"></a><span data-ttu-id="03d32-131">10012</span><span class="sxs-lookup"><span data-stu-id="03d32-131">10012</span></span>
<span data-ttu-id="03d32-132">エンティティを作成または更新できません。ノートブックが含まれるライブラリの場合、アイテムを編集する前にチェックアウトする必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="03d32-132">Unable to create or update the entity because the library that contains the notebook requires items to be checked out before they can be edited.</span></span> <span data-ttu-id="03d32-133">詳細については、https://support.office.com/ja-jp/article/Configure-a-site-library-to-require-check-out-of-files-f63fcbdc-1db6-4eb7-a3eb-dd815500c9e7 を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-133">For more information, see https://support.office.com/en-us/article/Configure-a-site-library-to-require-check-out-of-files-f63fcbdc-1db6-4eb7-a3eb-dd815500c9e7.</span></span>

<span data-ttu-id="03d32-134">ライブラリからチェックアウト要件を削除するか、ノートブックを移動します。</span><span class="sxs-lookup"><span data-stu-id="03d32-134">Either remove the check-out requirement from the library, or move the notebook.</span></span>

### <a name="10013"></a><span data-ttu-id="03d32-135">10013</span><span class="sxs-lookup"><span data-stu-id="03d32-135">10013</span></span>
<span data-ttu-id="03d32-136">ユーザーまたはグループの OneDrive にある 1 つ以上のドキュメント ライブラリに 20,000 を超えるアイテムが含まれており、API を使用してクエリ用にインデックス付けをすることができません。</span><span class="sxs-lookup"><span data-stu-id="03d32-136">One or more of the document libraries on the user or group's OneDrive contains more than 5000 OneNote items (notebooks, sections, section groups), and cannot be queried using the API.</span></span> <span data-ttu-id="03d32-137">ユーザーまたはグループのどのドキュメント ライブラリについても、その中のアイテム数が 20,000 を超えることがないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="03d32-137">Please make sure that none of the user or group's document libraries contains more than 5000 OneNote items.</span></span> <span data-ttu-id="03d32-138">軽減の手順については「[OneNote 開発者ブログ](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-138">See the [OneNote Dev blog](https://blogs.msdn.microsoft.com/onenotedev/2016/09/11/onenote-api-calls-fail-with-a-large-number-of-items-in-a-sharepoint-document-library/) for mitigation steps.</span></span>

### <a name="10014"></a><span data-ttu-id="03d32-139">10014</span><span class="sxs-lookup"><span data-stu-id="03d32-139">10014</span></span>
<span data-ttu-id="03d32-140">現在、Azure Key Vault がビジー状態であるため、受信した要求を処理できません。</span><span class="sxs-lookup"><span data-stu-id="03d32-140">The server is too busy to handle the incoming request at this moment. Please try again later.</span></span> <span data-ttu-id="03d32-141">後でもう一度お試しください。</span><span class="sxs-lookup"><span data-stu-id="03d32-141">Please try again later.</span></span>

### <a name="10015"></a><span data-ttu-id="03d32-142">10015</span><span class="sxs-lookup"><span data-stu-id="03d32-142">10015</span></span>
<span data-ttu-id="03d32-143">SharePoint は現在利用できません。</span><span class="sxs-lookup"><span data-stu-id="03d32-143">SharePoint is currently unavailable.</span></span> <span data-ttu-id="03d32-144">後でもう一度お試しください。</span><span class="sxs-lookup"><span data-stu-id="03d32-144">Please try again later.</span></span>

### <a name="10016"></a><span data-ttu-id="03d32-145">10016</span><span class="sxs-lookup"><span data-stu-id="03d32-145">10016</span></span>
<span data-ttu-id="03d32-146">ユーザーまたはグループの OneDrive 上のドキュメント ライブラリで、固有のセキュリティ スコープのしきい値の制限を超えました。</span><span class="sxs-lookup"><span data-stu-id="03d32-146">Document library on the user or group’s OneDrive exceeded unique security scopes threshold limit.</span></span> <span data-ttu-id="03d32-147">ライブラリに設定する固有のセキュリティ スコープの最大数が、50,000 個を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="03d32-147">The maximum number of unique security scopes set for a library cannot exceed 50,000.</span></span>

### <a name="10017"></a><span data-ttu-id="03d32-148">10017</span><span class="sxs-lookup"><span data-stu-id="03d32-148">10017</span></span>
<span data-ttu-id="03d32-149">要求が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="03d32-149">Bad Request</span></span>

### <a name="19999"></a><span data-ttu-id="03d32-150">19999</span><span class="sxs-lookup"><span data-stu-id="03d32-150">19999</span></span>
<span data-ttu-id="03d32-151">未定義のエラーが発生したため、要求は失敗しました。</span><span class="sxs-lookup"><span data-stu-id="03d32-151">The request failed because an undetermined error occurred.</span></span>

## <a name="codes-from-20001-to-29999"></a><span data-ttu-id="03d32-152">20001 から 29999 のコード</span><span class="sxs-lookup"><span data-stu-id="03d32-152">Codes from 20001 to 29999</span></span>
<span data-ttu-id="03d32-153">アプリケーション コードが間違った処理を実行しました。</span><span class="sxs-lookup"><span data-stu-id="03d32-153">The application code has done something wrong.</span></span>

### <a name="20001"></a><span data-ttu-id="03d32-154">20001</span><span class="sxs-lookup"><span data-stu-id="03d32-154">20001</span></span>

<span data-ttu-id="03d32-155">要求に必須の "Presentation" パートがありません。</span><span class="sxs-lookup"><span data-stu-id="03d32-155">The request is missing the required "Presentation" part.</span></span> <span data-ttu-id="03d32-156">1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="03d32-156">Exactly one is required.</span></span> 

### <a name="20002"></a><span data-ttu-id="03d32-157">20002</span><span class="sxs-lookup"><span data-stu-id="03d32-157">20002</span></span>
<span data-ttu-id="03d32-158">要求に "Presentation" パートが 2 つ以上あります。</span><span class="sxs-lookup"><span data-stu-id="03d32-158">The request contains two or more "Presentation" parts.</span></span> <span data-ttu-id="03d32-159">1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="03d32-159">Exactly one is required.</span></span>

### <a name="20003"></a><span data-ttu-id="03d32-160">20003</span><span class="sxs-lookup"><span data-stu-id="03d32-160">20003</span></span>
<span data-ttu-id="03d32-161">"Presentation" パートのコンテンツ タイプは、text/HTML または application/XHTML+XML のいずれかでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="03d32-161">The content type of the "Presentation" part can be only text/html or application/xhtml+xml.</span></span> 

### <a name="20004"></a><span data-ttu-id="03d32-162">20004</span><span class="sxs-lookup"><span data-stu-id="03d32-162">20004</span></span>
<span data-ttu-id="03d32-163">"Presentation" パートの HTML に、**src** プロパティと **data-render-src** プロパティの両方が設定されている画像タグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-163">The "Presentation" part HTML contains an image tag with both the **src** and the **data-render-src** properties set.</span></span> <span data-ttu-id="03d32-164">API は **src** プロパティを無視し、**data-render-src** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="03d32-164">The API will ignore the **src** property and use the **data-render-src** property.</span></span> 

### <a name="20005"></a><span data-ttu-id="03d32-165">20005</span><span class="sxs-lookup"><span data-stu-id="03d32-165">20005</span></span>
<span data-ttu-id="03d32-p114">要求の URI が長すぎます。URI の最大サイズ (すべてのパラメーターとデータを含む) は 16 KB (16,384 文字) です。</span><span class="sxs-lookup"><span data-stu-id="03d32-p114">The request URI is too long. The maximum size of the URI (including all parameters and data) is 16 KB or 16,384 characters.</span></span>

### <a name="20006"></a><span data-ttu-id="03d32-168">20006</span><span class="sxs-lookup"><span data-stu-id="03d32-168">20006</span></span>
<span data-ttu-id="03d32-169">"Presentation" パートの HTML に、src プロパティと **data-render-src** プロパティのいずれかが設定されている画像タグが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-169">The "Presentation" part HTML contains an image tag with neither the src nor the **data-render-src** properties set.</span></span> <span data-ttu-id="03d32-170">API は **image** タグを無視します。</span><span class="sxs-lookup"><span data-stu-id="03d32-170">The API will ignore the **image** tag.</span></span> 

### <a name="20007"></a><span data-ttu-id="03d32-171">20007</span><span class="sxs-lookup"><span data-stu-id="03d32-171">20007</span></span>
<span data-ttu-id="03d32-172">"Presentation" パートの HTML に含まれる作成日時の文字列が、許可される形式のいずれとも一致しません。</span><span class="sxs-lookup"><span data-stu-id="03d32-172">The "Presentation" part HTML contains a created date/time string that does not match any of the allowed formats.</span></span> 

### <a name="20008"></a><span data-ttu-id="03d32-173">20008</span><span class="sxs-lookup"><span data-stu-id="03d32-173">20008</span></span>
<span data-ttu-id="03d32-174">要求のサイズが大きすぎます。</span><span class="sxs-lookup"><span data-stu-id="03d32-174">The size of the request is too large.</span></span> 

### <a name="20009"></a><span data-ttu-id="03d32-175">20009</span><span class="sxs-lookup"><span data-stu-id="03d32-175">20009</span></span>
<span data-ttu-id="03d32-176">要求のパートに名前が重複しているものがあります。</span><span class="sxs-lookup"><span data-stu-id="03d32-176">The request contains parts with duplicate names.</span></span> <span data-ttu-id="03d32-177">パートの名前は一意にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d32-177">Part names must be unique.</span></span> 

### <a name="20010"></a><span data-ttu-id="03d32-178">20010</span><span class="sxs-lookup"><span data-stu-id="03d32-178">20010</span></span>
<span data-ttu-id="03d32-179">指定のコンテンツ タイプには Content-Disposition ヘッダーが指定されていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-179">The Content-Disposition header was not supplied for the specified content type.</span></span> 

### <a name="20011"></a><span data-ttu-id="03d32-180">20011</span><span class="sxs-lookup"><span data-stu-id="03d32-180">20011</span></span>
<span data-ttu-id="03d32-181">要求にはマルチパート ペイロードが含まれていますが、その形式が不正です。</span><span class="sxs-lookup"><span data-stu-id="03d32-181">The request contains a malformed multipart payload.</span></span> <span data-ttu-id="03d32-182">空白行がない、最後の行がない、パートの区切りの書式が正しくないなどの問題が考えられます。</span><span class="sxs-lookup"><span data-stu-id="03d32-182">Problems could include missing blank lines, a missing last line, incorrectly formatted part separators, and so on.</span></span> <span data-ttu-id="03d32-183">マルチパート メッセージを手動で作成する場合、ロジックを注意深く確認するか、サードパーティ ライブラリの使用をご検討ください。</span><span class="sxs-lookup"><span data-stu-id="03d32-183">If you're building the multipart message by hand, carefully check the logic, or consider using a third-party library.</span></span> 

### <a name="20012"></a><span data-ttu-id="03d32-184">20012</span><span class="sxs-lookup"><span data-stu-id="03d32-184">20012</span></span>
<span data-ttu-id="03d32-185">この要求は、指定のパートにコンテンツ タイプを指定しません。</span><span class="sxs-lookup"><span data-stu-id="03d32-185">The request doesn't supply a content type for the specified part.</span></span> 
### <a name="20013"></a><span data-ttu-id="03d32-186">20013</span><span class="sxs-lookup"><span data-stu-id="03d32-186">20013</span></span>
<span data-ttu-id="03d32-187">要求の中で、指定したパートの Content-Type ヘッダーおよび Content-Disposition ヘッダーが提供されていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-187">The request doesn't supply Content-Type and Content-Disposition headers for the specified part.</span></span> 

### <a name="20014"></a><span data-ttu-id="03d32-188">20014</span><span class="sxs-lookup"><span data-stu-id="03d32-188">20014</span></span>
<span data-ttu-id="03d32-189">マルチパート メッセージのパートの長さが最大サイズである 25 MB を超えています。</span><span class="sxs-lookup"><span data-stu-id="03d32-189">The length of a part in the multipart message exceeds the maximum size of 25 MB.</span></span> 

### <a name="20015"></a><span data-ttu-id="03d32-190">20015</span><span class="sxs-lookup"><span data-stu-id="03d32-190">20015</span></span>
<span data-ttu-id="03d32-191">マルチパート メッセージのパート数が上限の 500 を超えています。</span><span class="sxs-lookup"><span data-stu-id="03d32-191">The count of parts in the multipart message exceeds the limit of 30.</span></span> 

### <a name="20016"></a><span data-ttu-id="03d32-192">20016</span><span class="sxs-lookup"><span data-stu-id="03d32-192">20016</span></span>
<span data-ttu-id="03d32-193">マルチパート メッセージの長さが上限の 75 MB を超えています。</span><span class="sxs-lookup"><span data-stu-id="03d32-193">The length of the multipart message exceeds the limit of 70 MB.</span></span> 

### <a name="20017"></a><span data-ttu-id="03d32-194">20017</span><span class="sxs-lookup"><span data-stu-id="03d32-194">20017</span></span>
<span data-ttu-id="03d32-195">電子メールの MIME の形式が正しくありませんでした。</span><span class="sxs-lookup"><span data-stu-id="03d32-195">The email MIME was malformed.</span></span> 

### <a name="20018"></a><span data-ttu-id="03d32-196">20018</span><span class="sxs-lookup"><span data-stu-id="03d32-196">20018</span></span>
<span data-ttu-id="03d32-197">会議の MIME または ICal の形式が正しくありませんでした。</span><span class="sxs-lookup"><span data-stu-id="03d32-197">The meeting MIME or ICal was malformed.</span></span> 

### <a name="20019"></a><span data-ttu-id="03d32-198">20019</span><span class="sxs-lookup"><span data-stu-id="03d32-198">20019</span></span>
<span data-ttu-id="03d32-199">ICal は見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="03d32-199">No ICal was found.</span></span> 

### <a name="20020"></a><span data-ttu-id="03d32-200">20020</span><span class="sxs-lookup"><span data-stu-id="03d32-200">20020</span></span>
<span data-ttu-id="03d32-201">要求の本文に無効な形式の Json がありました。</span><span class="sxs-lookup"><span data-stu-id="03d32-201">Encountered malformed Json in request body.</span></span> 

### <a name="20100"></a><span data-ttu-id="03d32-202">20100</span><span class="sxs-lookup"><span data-stu-id="03d32-202">20100</span></span>
<span data-ttu-id="03d32-203">要求の構文に誤りがあります。</span><span class="sxs-lookup"><span data-stu-id="03d32-203">Something is wrong with the syntax of your request.</span></span> 
### <a name="20101"></a><span data-ttu-id="03d32-204">20101</span><span class="sxs-lookup"><span data-stu-id="03d32-204">20101</span></span>
<span data-ttu-id="03d32-205">要求したプロパティは存在しません。</span><span class="sxs-lookup"><span data-stu-id="03d32-205">The property that you requested doesn't exist.</span></span>

### <a name="20102"></a><span data-ttu-id="03d32-206">20102</span><span class="sxs-lookup"><span data-stu-id="03d32-206">20102</span></span>
<span data-ttu-id="03d32-207">存在しないリソースが要求されました。</span><span class="sxs-lookup"><span data-stu-id="03d32-207">You requested a resource that doesn't exist.</span></span>

### <a name="20103"></a><span data-ttu-id="03d32-208">20103</span><span class="sxs-lookup"><span data-stu-id="03d32-208">20103</span></span>
<span data-ttu-id="03d32-209">**expand** クエリはこの要求ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="03d32-209">The **expand** query is not supported for this request.</span></span> <span data-ttu-id="03d32-210">「[サポートされる OData クエリ文字列オプション](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content#query-options)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-210">See [Supported OData query string options](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content#query-options).</span></span>

### <a name="20104"></a><span data-ttu-id="03d32-211">20104</span><span class="sxs-lookup"><span data-stu-id="03d32-211">20104 (SectionNameInvalidChar)</span></span>
<span data-ttu-id="03d32-212">**pagelevel** クエリ オプションは、セクションにあるページ コレクションまたは特定のページに対してクエリを行うときだけサポートされます。</span><span class="sxs-lookup"><span data-stu-id="03d32-212">The **pagelevel** query option is supported only when querying for the pages collection in a section or for a specific page.</span></span> <span data-ttu-id="03d32-213">たとえば次のようにします。</span><span class="sxs-lookup"><span data-stu-id="03d32-213">For example:</span></span>  

```http
GET ../sections/{id}/pages?pagelevel=true
GET ../pages/{id}?pagelevel=true
```

### <a name="20106"></a><span data-ttu-id="03d32-214">20106</span><span class="sxs-lookup"><span data-stu-id="03d32-214">20106</span></span>
<span data-ttu-id="03d32-215">要求に、サポートされていないクエリ演算子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-215">Your request contains a query operator that is not supported.</span></span> 

### <a name="20108"></a><span data-ttu-id="03d32-216">20108</span><span class="sxs-lookup"><span data-stu-id="03d32-216">20108</span></span>
<span data-ttu-id="03d32-217">要求に、サポートされていない OData クエリ パラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-217">Your request contains unsupported OData query parameters.</span></span>

### <a name="20109"></a><span data-ttu-id="03d32-218">20109</span><span class="sxs-lookup"><span data-stu-id="03d32-218">20109</span></span>
<span data-ttu-id="03d32-219">PATCH 要求内のペイロードの構成が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="03d32-219">The payload in the PATCH request is not constructed correctly.</span></span>

### <a name="20110"></a><span data-ttu-id="03d32-220">20110</span><span class="sxs-lookup"><span data-stu-id="03d32-220">20110</span></span>
<span data-ttu-id="03d32-221">データ パートを伴うページ作成要求では、コンテンツが "Presentation" パートを含むマルチパートである必要があります。</span><span class="sxs-lookup"><span data-stu-id="03d32-221">Page create requests with data parts require the content to be multipart, with a "Presentation" part.</span></span> 

### <a name="20111"></a><span data-ttu-id="03d32-222">20111</span><span class="sxs-lookup"><span data-stu-id="03d32-222">20111</span></span>
<span data-ttu-id="03d32-223">要求で使用されている OData 機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-223">Your request uses an OData feature that isn't supported.</span></span>

### <a name="20112"></a><span data-ttu-id="03d32-224">20112</span><span class="sxs-lookup"><span data-stu-id="03d32-224">20112</span></span>
<span data-ttu-id="03d32-225">ターゲット ノートブック、セクション グループ、セクション、またはページ エンティティの無効な ID が要求に含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-225">Your request contains an invalid ID for the target notebook, section group, section, or page entity.</span></span>

### <a name="20113"></a><span data-ttu-id="03d32-226">20113</span><span class="sxs-lookup"><span data-stu-id="03d32-226">20113</span></span>
<span data-ttu-id="03d32-227">要求で指定されているリソースは削除されました。</span><span class="sxs-lookup"><span data-stu-id="03d32-227">The resource specified in the request has been deleted.</span></span>

### <a name="20115"></a><span data-ttu-id="03d32-228">20115</span><span class="sxs-lookup"><span data-stu-id="03d32-228">20115</span></span>
<span data-ttu-id="03d32-229">名前に無効な文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-229">The name contains invalid characters.</span></span> <span data-ttu-id="03d32-230">ノートブック名には次の文字を含めることはできません: `? * \ / : < > | ' "`</span><span class="sxs-lookup"><span data-stu-id="03d32-230">A notebook name cannot contain any of the following characters: `? * \ / : < > | ' "`</span></span>

### <a name="20117"></a><span data-ttu-id="03d32-231">20117</span><span class="sxs-lookup"><span data-stu-id="03d32-231">20117</span></span>
<span data-ttu-id="03d32-232">指定された名前のアイテムは、指定された場所に既に存在します。</span><span class="sxs-lookup"><span data-stu-id="03d32-232">An item with the name you specified already exists in the location that you specified.</span></span>

### <a name="20119"></a><span data-ttu-id="03d32-233">20119</span><span class="sxs-lookup"><span data-stu-id="03d32-233">20119</span></span>
<span data-ttu-id="03d32-234">"Presentation" パートの HTML に含まれる **data-attachment** 属性の形式が無効であるか、またはファイル名には無効な文字 (`\ / : * ? < > | "`) が 1 つ以上含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-234">The HTML in the "Presentation" part contains a **data-attachment** attribute that either doesn't have a valid format or includes one or more of these invalid characters for a file name: `\ / : * ? < > | "`.</span></span> <span data-ttu-id="03d32-235">要求では、エラー メッセージに示されている値に置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="03d32-235">The request substituted the value indicated in the error message.</span></span>

### <a name="20120"></a><span data-ttu-id="03d32-236">20120</span><span class="sxs-lookup"><span data-stu-id="03d32-236">20120</span></span>
<span data-ttu-id="03d32-237">要求で指定された PATCH ターゲットが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="03d32-237">Your request specifies a PATCH target that can't be located.</span></span>

### <a name="20121"></a><span data-ttu-id="03d32-238">20121</span><span class="sxs-lookup"><span data-stu-id="03d32-238">20121</span></span>
<span data-ttu-id="03d32-239">要求に含まれている PATCH 引数が無効です。</span><span class="sxs-lookup"><span data-stu-id="03d32-239">Your request contains an invalid PATCH argument.</span></span> <span data-ttu-id="03d32-240">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-240">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20122"></a><span data-ttu-id="03d32-241">20122</span><span class="sxs-lookup"><span data-stu-id="03d32-241">20122</span></span>
<span data-ttu-id="03d32-242">要求で指定されている PATCH アクションはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-242">Your request specifies an unsupported PATCH action.</span></span> <span data-ttu-id="03d32-243">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-243">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20123"></a><span data-ttu-id="03d32-244">20123</span><span class="sxs-lookup"><span data-stu-id="03d32-244">20123</span></span>
<span data-ttu-id="03d32-245">PATCH 要求は、指定されたページを変更できません。</span><span class="sxs-lookup"><span data-stu-id="03d32-245">The PATCH request is unable to alter the specified page.</span></span>

### <a name="20124"></a><span data-ttu-id="03d32-246">20124</span><span class="sxs-lookup"><span data-stu-id="03d32-246">20124</span></span>
<span data-ttu-id="03d32-247">マルチパートの PATCH 要求に、PATCH アクションの JSON 構造を指定した "commands" パートが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-247">Your multipart PATCH request doesn't include a "commands" part with the PATCH action JSON structure.</span></span> <span data-ttu-id="03d32-248">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-248">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20125"></a><span data-ttu-id="03d32-249">20125</span><span class="sxs-lookup"><span data-stu-id="03d32-249">20125</span></span>
<span data-ttu-id="03d32-250">PATCH 要求にアクションが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-250">Your PATCH request contains no actions.</span></span> <span data-ttu-id="03d32-251">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-251">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20126"></a><span data-ttu-id="03d32-252">20126</span><span class="sxs-lookup"><span data-stu-id="03d32-252">20126</span></span>
<span data-ttu-id="03d32-253">メッセージ本文に、不正な書式設定の JSON またはこの操作に対してはサポートされていないフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-253">The message body contains either incorrectly formatted JSON or fields that are not supported for this operation.</span></span>

### <a name="20127"></a><span data-ttu-id="03d32-254">20127</span><span class="sxs-lookup"><span data-stu-id="03d32-254">20127</span></span>
<span data-ttu-id="03d32-255">要求で指定された名前は不明なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="03d32-255">Your request specifies the name of an unknown property.</span></span>

### <a name="20128"></a><span data-ttu-id="03d32-256">20128</span><span class="sxs-lookup"><span data-stu-id="03d32-256">20128</span></span>
<span data-ttu-id="03d32-257">要求に含まれている OData で、メッセージに示されている位置に構文エラーがあります。</span><span class="sxs-lookup"><span data-stu-id="03d32-257">Your request contains an OData syntax error at the position indicated in the message.</span></span>

### <a name="20129"></a><span data-ttu-id="03d32-258">20129</span><span class="sxs-lookup"><span data-stu-id="03d32-258">20129</span></span>
<span data-ttu-id="03d32-259">要求に、値が大きすぎる **top** クエリ文字列オプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="03d32-259">Your request contains a $top query whose value is too high.</span></span> <span data-ttu-id="03d32-260">ページのクエリの場合、最大値は 100 で、既定値は 20 です。</span><span class="sxs-lookup"><span data-stu-id="03d32-260">Your request contains a top query string option whose value is too high. For page queries, the maximum value is 100, and the default value is 20.</span></span>

### <a name="20130"></a><span data-ttu-id="03d32-261">20130</span><span class="sxs-lookup"><span data-stu-id="03d32-261">20130</span></span>
<span data-ttu-id="03d32-262">要求に含まれている URI が指している HTTP リソースが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="03d32-262">Your request contains a URI that points to an HTTP resource that can't be found.</span></span>

### <a name="20131"></a><span data-ttu-id="03d32-263">20131</span><span class="sxs-lookup"><span data-stu-id="03d32-263">20131</span></span>
<span data-ttu-id="03d32-264">要求に Content-Type の無効な値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-264">Your request contains an invalid value for Content-Type.</span></span> <span data-ttu-id="03d32-265">メッセージに指定されている値を使用します。</span><span class="sxs-lookup"><span data-stu-id="03d32-265">Use the value indicated in the message.</span></span> 

### <a name="20132"></a><span data-ttu-id="03d32-266">20132</span><span class="sxs-lookup"><span data-stu-id="03d32-266">20132</span></span>
<span data-ttu-id="03d32-267">要求に無効なコンテンツが含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-267">Your request contains invalid content.</span></span> <span data-ttu-id="03d32-268">このエラーのよくある原因は、Content-Type 要求ヘッダーの欠落や、要求の本文にコンテンツが含まれていないことです。</span><span class="sxs-lookup"><span data-stu-id="03d32-268">Common causes for this are a missing Content-Type request header and/or no content in the body of the request.</span></span> 

### <a name="20133"></a><span data-ttu-id="03d32-269">20133</span><span class="sxs-lookup"><span data-stu-id="03d32-269">20133</span></span>
<span data-ttu-id="03d32-270">要求で指定された PATCH ターゲットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-270">Your request specifies a PATCH target that is not supported.</span></span> <span data-ttu-id="03d32-271">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-271">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20134"></a><span data-ttu-id="03d32-272">20134</span><span class="sxs-lookup"><span data-stu-id="03d32-272">20134</span></span>
<span data-ttu-id="03d32-273">要求に、PATCH アクションのターゲットとして無効な要素が指定されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-273">Your request specifies an invalid element as the target of the PATCH action.</span></span> <span data-ttu-id="03d32-274">ターゲットで **data-id** 識別子が使用されている場合は、プレフィックスとして # 記号が付いていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-274">Your request specifies an invalid element as the target of the PATCH action. If the target uses the **data-id** identifier, make sure it's prefixed with a # symbol. See Update page content.</span></span> <span data-ttu-id="03d32-275">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-275">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20135"></a><span data-ttu-id="03d32-276">20135</span><span class="sxs-lookup"><span data-stu-id="03d32-276">20135</span></span>
<span data-ttu-id="03d32-277">要求に指定されたエンティティの種類は、PATCH 操作に対してはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-277">Your request specifies an entity type that is not supported for the PATCH operation.</span></span> <span data-ttu-id="03d32-278">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-278">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20136"></a><span data-ttu-id="03d32-279">20136</span><span class="sxs-lookup"><span data-stu-id="03d32-279">20136</span></span>
<span data-ttu-id="03d32-280">要求に無効または不足している **data-render-src** または **data-render-method** 属性が含まれます。</span><span class="sxs-lookup"><span data-stu-id="03d32-280">Your request contains an invalid or missing **data-render-src** or **data-render-method** attribute.</span></span> <span data-ttu-id="03d32-281">「[キャプチャからのデータの抽出](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-extract-data)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-281">See [Extract data from captures](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-extract-data).</span></span>

### <a name="20137"></a><span data-ttu-id="03d32-282">20137</span><span class="sxs-lookup"><span data-stu-id="03d32-282">20137</span></span>
<span data-ttu-id="03d32-283">このターゲット ページにおいて、PATCH 要求はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-283">The target page does not support PATCH requests.</span></span>

### <a name="20138"></a><span data-ttu-id="03d32-284">20138</span><span class="sxs-lookup"><span data-stu-id="03d32-284">20138</span></span>
<span data-ttu-id="03d32-285">PATCH 要求のターゲット要素の種類では、**append** 操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-285">The target element type in your PATCH request doesn't support the **append** action.</span></span> <span data-ttu-id="03d32-286">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-286">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20139"></a><span data-ttu-id="03d32-287">20139</span><span class="sxs-lookup"><span data-stu-id="03d32-287">20139</span></span>
<span data-ttu-id="03d32-288">要求に、無効な **data-tag** 属性値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-288">Your request contains an invalid **data-tag** attribute value.</span></span> <span data-ttu-id="03d32-289">「[ノート シールを使用する](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-note-tags)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-289">See [Use note tags](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-note-tags).</span></span>

### <a name="20140"></a><span data-ttu-id="03d32-290">20140</span><span class="sxs-lookup"><span data-stu-id="03d32-290">20140</span></span>
<span data-ttu-id="03d32-291">要求に、無効な **data-tag** ステータス値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-291">Your request contains an invalid **data-tag** status value.</span></span> <span data-ttu-id="03d32-292">チェック ボックスのノート シールには、**completed** ステータスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="03d32-292">Check box note tags can have a **completed** status.</span></span> <span data-ttu-id="03d32-293">例:</span><span class="sxs-lookup"><span data-stu-id="03d32-293">Example:</span></span>
```html
    <p data-tag="to-do:completed">To-do note tag in completed state (checked box in the UI)</p>
```
<span data-ttu-id="03d32-294">「[ノート シールを使用する](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-note-tags)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-294">See [Use note tags](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-note-tags).</span></span>

### <a name="20141"></a><span data-ttu-id="03d32-295">20141</span><span class="sxs-lookup"><span data-stu-id="03d32-295">20141</span></span>
<span data-ttu-id="03d32-296">PATCH 要求のターゲット要素の種類では、指定の操作はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-296">The target in your PATCH request doesn't support the specified action.</span></span> <span data-ttu-id="03d32-297">「[ページ コンテンツの更新](../api-reference/v1.0/api/page_update.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-297">See [Update page content](../api-reference/v1.0/api/page_update.md).</span></span>

### <a name="20142"></a><span data-ttu-id="03d32-298">20142</span><span class="sxs-lookup"><span data-stu-id="03d32-298">20142</span></span>
<span data-ttu-id="03d32-299">要求に、子エンティティの親、または親エンティティの子に対する **expand** 式が含まれていますが、それはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-299">Your request contains an **expand** expression for a parent of child entities or a child of parent entities, which  is not supported. See Supported OData query options.</span></span> <span data-ttu-id="03d32-300">「[サポートされる OData クエリ文字列オプション](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content#query-options)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-300">See [Supported OData query string options](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-get-content#query-options).</span></span>

### <a name="20143"></a><span data-ttu-id="03d32-301">20143</span><span class="sxs-lookup"><span data-stu-id="03d32-301">20143</span></span>
<span data-ttu-id="03d32-302">OData クエリが無効です。</span><span class="sxs-lookup"><span data-stu-id="03d32-302">The OData query is invalid.</span></span>

### <a name="20144"></a><span data-ttu-id="03d32-303">20144</span><span class="sxs-lookup"><span data-stu-id="03d32-303">20144</span></span>
<span data-ttu-id="03d32-304">要求に、ナビゲートでないプロパティに対する **expand** 式が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-304">Your request contains an **expand** expression for a non-navigation property.</span></span> <span data-ttu-id="03d32-305">展開できるのは、ナビゲート プロパティだけです。</span><span class="sxs-lookup"><span data-stu-id="03d32-305">Only navigation properties can be expanded.</span></span>

### <a name="20145"></a><span data-ttu-id="03d32-306">20145</span><span class="sxs-lookup"><span data-stu-id="03d32-306">20145</span></span>
<span data-ttu-id="03d32-307">要求の **select** 式または **expand** 式に、無効な用語が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-307">The **select** or **expand** expression in your request contains an invalid term.</span></span>

### <a name="20146"></a><span data-ttu-id="03d32-308">20146</span><span class="sxs-lookup"><span data-stu-id="03d32-308">20146</span></span>
<span data-ttu-id="03d32-309">要素で `style="position:absolute"` 属性が指定されていますが、**body** 要素で `data-absolute-enabled="true"` が指定されていません。この指定は、配置をサポートするためには必須です。</span><span class="sxs-lookup"><span data-stu-id="03d32-309">The `style="position:absolute"` attribute is specified on an element, but the **body** element does not specify `data-absolute-enabled="true"`, which is required to support positioning.</span></span> <span data-ttu-id="03d32-310">すべての位置設定が無視されます。</span><span class="sxs-lookup"><span data-stu-id="03d32-310">All position settings will be ignored.</span></span> <span data-ttu-id="03d32-311">「[絶対位置で配置された要素の作成](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-311">See [Create absolute positioned elements](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos).</span></span>

### <a name="20147"></a><span data-ttu-id="03d32-312">20147</span><span class="sxs-lookup"><span data-stu-id="03d32-312">20147</span></span>
<span data-ttu-id="03d32-313">サポートされていない **body** 要素の直接の子ではない要素で `style="position:absolute"` 属性が指定されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-313">The `style="position:absolute"` attribute is specified on an element that is not a direct child of the **body** element, which is not supported.</span></span> <span data-ttu-id="03d32-314">要素が **div**、**img**、**object** の場合、それを body の直接の子にします。直接の子にしない場合、位置設定が無視され、絶対位置で配置された div の中でそのコンテンツがレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="03d32-314">If the element is a **div**, **img**, or **object**, make it a direct child of the body; otherwise the position settings will be ignored and its content will render inside an absolute positioned div.</span></span> <span data-ttu-id="03d32-315">「[絶対位置で配置された要素の作成](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-315">See [Create absolute positioned elements](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos).</span></span>

### <a name="20148"></a><span data-ttu-id="03d32-316">20148</span><span class="sxs-lookup"><span data-stu-id="03d32-316">20148</span></span>
<span data-ttu-id="03d32-317">`style="position:absolute"` 属性がそれをサポートしない種類の要素で指定されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-317">The `style="position:absolute"` attribute is specified on an element type that does not support it.</span></span> <span data-ttu-id="03d32-318">ページ本文の直接の子である **div**、**img**、**object** 要素だけが位置設定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="03d32-318">Only **div**, **img**, and **object** elements that are direct children of the page body support positioning.</span></span> <span data-ttu-id="03d32-319">「[絶対位置で配置された要素の作成](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-319">See [Create absolute positioned elements](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-abs-pos).</span></span>

### <a name="20149"></a><span data-ttu-id="03d32-320">20149</span><span class="sxs-lookup"><span data-stu-id="03d32-320">20149</span></span>
<span data-ttu-id="03d32-321">要求が指定しているターゲット要素が見つかりません。</span><span class="sxs-lookup"><span data-stu-id="03d32-321">Your request specifies a target element that cannot be found.</span></span>

### <a name="20150"></a><span data-ttu-id="03d32-322">20150</span><span class="sxs-lookup"><span data-stu-id="03d32-322">20150</span></span>
<span data-ttu-id="03d32-323">この認証の種類には、この要求は無効です。</span><span class="sxs-lookup"><span data-stu-id="03d32-323">The request is not valid for this authentication type.</span></span> <span data-ttu-id="03d32-324">代わりに、`../me/onenote/` パスを使用してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-324">Use the `../me/onenote/` path instead.</span></span>

### <a name="20151"></a><span data-ttu-id="03d32-325">20151</span><span class="sxs-lookup"><span data-stu-id="03d32-325">20151</span></span>
<span data-ttu-id="03d32-326">この認証の種類には、この要求は無効です。</span><span class="sxs-lookup"><span data-stu-id="03d32-326">The request is not valid for this authentication type.</span></span> <span data-ttu-id="03d32-327">`../me/onenote/section/{id}/pages` エンドポイントを使用し、特定のセクションにページを作成します。</span><span class="sxs-lookup"><span data-stu-id="03d32-327">Use the `../me/onenote/section/{id}/pages` endpoint to create a page in a specific section.</span></span>

### <a name="20152"></a><span data-ttu-id="03d32-328">20152</span><span class="sxs-lookup"><span data-stu-id="03d32-328">20152 (EntityNameEmpty)</span></span>
<span data-ttu-id="03d32-p144">エンティティに指定されている名前値がありません。この名前を定義する必要があります。空白のみを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="03d32-p144">There is no name value specified for the entity. The name must be defined, and it cannot contain whitespaces only.</span></span>

### <a name="20153"></a><span data-ttu-id="03d32-331">20153</span><span class="sxs-lookup"><span data-stu-id="03d32-331">20153 (EntityNameInvalidChar)</span></span>
<span data-ttu-id="03d32-332">エンティティ名に使用できない文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03d32-332">The entity name contains invalid characters.</span></span> <span data-ttu-id="03d32-333">名前には、以下の文字を含めることはできません: `? * \ / : < > | & # " % ~`</span><span class="sxs-lookup"><span data-stu-id="03d32-333">The name cannot contain the following characters: `? * \ / : < > | & # " % ~`</span></span>

### <a name="20154"></a><span data-ttu-id="03d32-334">20154</span><span class="sxs-lookup"><span data-stu-id="03d32-334">20154 (EntityNameInvalidStart)</span></span>
<span data-ttu-id="03d32-335">エンティティ名を空白で始めることはできません。</span><span class="sxs-lookup"><span data-stu-id="03d32-335">The entity name cannot start with a space.</span></span>

### <a name="20155"></a><span data-ttu-id="03d32-336">20155</span><span class="sxs-lookup"><span data-stu-id="03d32-336">20155 (EntityNameTooLong)</span></span>
<span data-ttu-id="03d32-p146">エンティティ名が長すぎます。ノートブック名には 128 文字の制限があります。他のエンティティ名には 50 文字の制限があります。</span><span class="sxs-lookup"><span data-stu-id="03d32-p146">The entity name is too long. Notebook names have a 128-character limit. Other entity names have a 50-character limit.</span></span>

### <a name="20156"></a><span data-ttu-id="03d32-340">20156</span><span class="sxs-lookup"><span data-stu-id="03d32-340">20156</span></span>
<span data-ttu-id="03d32-341">宛先リソースの指定された ID が存在しません。</span><span class="sxs-lookup"><span data-stu-id="03d32-341">The specified ID for the destination resource does not exist.</span></span>

### <a name="20157"></a><span data-ttu-id="03d32-342">20157</span><span class="sxs-lookup"><span data-stu-id="03d32-342">20157</span></span>
<span data-ttu-id="03d32-343">宛先エンティティの指定された ID が無効です。</span><span class="sxs-lookup"><span data-stu-id="03d32-343">The specified ID for the destination entity is invalid.</span></span>

### <a name="20158"></a><span data-ttu-id="03d32-344">20158</span><span class="sxs-lookup"><span data-stu-id="03d32-344">20158</span></span>
<span data-ttu-id="03d32-345">要求に指定されているサイト URL のメタデータを取得できません。</span><span class="sxs-lookup"><span data-stu-id="03d32-345">Unable to get metadata for the site URL specified in the request.</span></span> <span data-ttu-id="03d32-346">指定された URL の形式を確認してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-346">Check the format of the supplied URL.</span></span> <span data-ttu-id="03d32-347">サポートされている形式は `https://domain.sharepoint.com/site-a` と `https://domain.com/sites/site-a` です。</span><span class="sxs-lookup"><span data-stu-id="03d32-347">Supported formats include `https://domain.sharepoint.com/site-a` and `https://domain.com/sites/site-a`.</span></span>

### <a name="20160"></a><span data-ttu-id="03d32-348">20160</span><span class="sxs-lookup"><span data-stu-id="03d32-348">20160</span></span>
<span data-ttu-id="03d32-349">指定した ID を持つ Office 365 統合グループを見つけることができません。</span><span class="sxs-lookup"><span data-stu-id="03d32-349">Unable to find an Office 365 unified group that has the specified ID.</span></span>

### <a name="20161"></a><span data-ttu-id="03d32-350">20161</span><span class="sxs-lookup"><span data-stu-id="03d32-350">20161</span></span>
<span data-ttu-id="03d32-p148">コンテキストで、有効なユーザー ID が指定されていません。一般的なエラーの 1 つとして、PUID/CID が 16 進数ではなく long 型として渡されたことが挙げられます。</span><span class="sxs-lookup"><span data-stu-id="03d32-p148">The context does not specify a valid user ID. One common error is that PUID/CID was passed in as a long instead of a hex.</span></span>

### <a name="20166"></a><span data-ttu-id="03d32-353">20166</span><span class="sxs-lookup"><span data-stu-id="03d32-353">20166</span></span>
<span data-ttu-id="03d32-354">アプリケーションは、短時間に非常に多くの要求をユーザーの代理で発行しました。</span><span class="sxs-lookup"><span data-stu-id="03d32-354">The application has issued too many requests on behalf of a user in a short period of time.</span></span> <span data-ttu-id="03d32-355">OneNote API の安定性と応答性を保つために、アプリケーションがリソースを消費しすぎることが検出されると、API は 429 ステータス コードとこのエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="03d32-355">The application has issued too many requests on behalf of a user in a short period of time. To help ensure that the OneNote API remains stable and responsive, the API returns a 429 status code and this error when it detects that an application is using too many resources. For more information, see OneNote API throttling and how to avoid it.</span></span> 

<span data-ttu-id="03d32-356">詳細については、「[OneNote API の調整とその回避方法](http://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-356">For more information, see [OneNote API throttling and how to avoid it](http://blogs.msdn.com/b/onenotedev/archive/2016/01/13/onenote-api-throttling-and-best-practices.aspx).</span></span>

### <a name="20168"></a><span data-ttu-id="03d32-357">20168</span><span class="sxs-lookup"><span data-stu-id="03d32-357">20168</span></span>
<span data-ttu-id="03d32-358">要求に指定されているビデオ ソースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-358">The video source specified in the request is not supported.</span></span> <span data-ttu-id="03d32-359">現行の一覧については、「[サポートされているビデオ サイト](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-images-files#videos)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-359">See [Supported video sites](https://msdn.microsoft.com/en-us/office/office365/howto/onenote-images-files#videos) for the current list.</span></span>


## <a name="codes-from-30001-to-39999"></a><span data-ttu-id="03d32-360">30001 から 39999 のコード</span><span class="sxs-lookup"><span data-stu-id="03d32-360">Codes from 30001 to 39999</span></span>
<span data-ttu-id="03d32-361">ユーザーのアカウントに問題があります。</span><span class="sxs-lookup"><span data-stu-id="03d32-361">Something is wrong with the user's account.</span></span>

### <a name="30101"></a><span data-ttu-id="03d32-362">30101</span><span class="sxs-lookup"><span data-stu-id="03d32-362">30101</span></span>
<span data-ttu-id="03d32-363">ユーザー アカウントは、その OneDrive のクォータを超えています。</span><span class="sxs-lookup"><span data-stu-id="03d32-363">The user account has exceeded its OneDrive quota.</span></span> <span data-ttu-id="03d32-364">「[OneDrive](https://onedrive.live.com/about/en-us/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-364">See [OneDrive](https://onedrive.live.com/about/en-us/).</span></span>

### <a name="30102"></a><span data-ttu-id="03d32-365">30102</span><span class="sxs-lookup"><span data-stu-id="03d32-365">30102</span></span>
<span data-ttu-id="03d32-366">要求されたセクションは、最大サイズに達したため、これ以上追加できません。</span><span class="sxs-lookup"><span data-stu-id="03d32-366">Nothing more can be added to the requested section because it has reached its maximum size.</span></span>

### <a name="30103"></a><span data-ttu-id="03d32-367">30103</span><span class="sxs-lookup"><span data-stu-id="03d32-367">30103</span></span>
<span data-ttu-id="03d32-p152">要求に対するリソース消費量が多すぎます。対象のユーザー アカウントに大きいデータセットが含まれているか、サービスが同じサイト (ユーザーの個人用サイトやチーム サイトなど) に対する多数の要求を同時に受信しています。</span><span class="sxs-lookup"><span data-stu-id="03d32-p152">Resource consumption is too high for the request. Either the target user account has a large dataset, or the service is receiving a high number of concurrent requests to the same site (for example, the user's personal site or a team site).</span></span>

### <a name="30104"></a><span data-ttu-id="03d32-370">30104</span><span class="sxs-lookup"><span data-stu-id="03d32-370">30104</span></span>
<span data-ttu-id="03d32-371">ユーザー アカウントが中断されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-371">The user account has been suspended.</span></span>

### <a name="30105"></a><span data-ttu-id="03d32-372">30105</span><span class="sxs-lookup"><span data-stu-id="03d32-372">30105</span></span>
<span data-ttu-id="03d32-p153">ノートブックにアクセスする必要がある、ユーザーの個人用 OneDrive for Business サイトがプロビジョニングされていません。OneNote サービスは今すぐサイトをプロビジョニングします。この処理には数分かかることがあります。</span><span class="sxs-lookup"><span data-stu-id="03d32-p153">The user's personal OneDrive for Business site is not provisioned, which is required to access notebooks. The OneNote service will provision the site now. This process may take several minutes.</span></span>

### <a name="30106"></a><span data-ttu-id="03d32-376">30106</span><span class="sxs-lookup"><span data-stu-id="03d32-376">30106</span></span>
<span data-ttu-id="03d32-377">OneDrive for Business は、ユーザーのためにプロビジョニング中です。</span><span class="sxs-lookup"><span data-stu-id="03d32-377">OneDrive for Business is being provisioned for the user.</span></span>

### <a name="30108"></a><span data-ttu-id="03d32-378">30108</span><span class="sxs-lookup"><span data-stu-id="03d32-378">30108</span></span>
<span data-ttu-id="03d32-379">ユーザーの個人用 OneDrive for Business を取得できませんでした。</span><span class="sxs-lookup"><span data-stu-id="03d32-379">The user's personal OneDrive for Business could not be retrieved. Here are some possible causes.</span></span> <span data-ttu-id="03d32-380">次の表に、いくつか考えられる原因を示します。</span><span class="sxs-lookup"><span data-stu-id="03d32-380">The following table lists some possible causes.</span></span>

| <span data-ttu-id="03d32-381">原因</span><span class="sxs-lookup"><span data-stu-id="03d32-381">Cause</span></span> | <span data-ttu-id="03d32-382">解決策</span><span class="sxs-lookup"><span data-stu-id="03d32-382">Resolution</span></span> |
|:------|:------|
| <span data-ttu-id="03d32-383">ユーザーの個人用サイトがプロビジョニングされていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-383">The user's personal site has not been provisioned.</span></span> | <span data-ttu-id="03d32-p155">ユーザーは、OneDrive for Business を開き、サイトをプロビジョニングするためのすべての指示に従います。これが失敗した場合は、Office 365 テナント管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="03d32-p155">The user should open OneDrive for Business and follow any instructions to provision the site. If this fails, they should contact their Office 365 tenant administrator.</span></span> |
| <span data-ttu-id="03d32-386">ユーザーの個人用サイトは現在プロビジョニング中です。</span><span class="sxs-lookup"><span data-stu-id="03d32-386">The user's personal site is currently being provisioned.</span></span> | <span data-ttu-id="03d32-387">後で要求を再試行してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-387">Try the request later.</span></span> |
| <span data-ttu-id="03d32-388">ユーザーは、有効な OneDrive for Business ライセンスを持っていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-388">The user does not have a valid OneDrive for Business license.</span></span> | <span data-ttu-id="03d32-389">Office 365 テナント管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="03d32-389">The user should contact their Office 365 tenant administrator.</span></span> |
| <span data-ttu-id="03d32-390">ネットワークの問題により、要求が正常に送信されていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-390">A network issue prevented the request from being successfully sent.</span></span> | <span data-ttu-id="03d32-391">後で要求をお試しください。</span><span class="sxs-lookup"><span data-stu-id="03d32-391">Try the request later.</span></span> |

### <a name="30109"></a><span data-ttu-id="03d32-392">30109</span><span class="sxs-lookup"><span data-stu-id="03d32-392">30109</span></span>
<span data-ttu-id="03d32-393">要求の一部のユーザーは存在しません。</span><span class="sxs-lookup"><span data-stu-id="03d32-393">Some users in the request do not exist.</span></span>

### <a name="30110"></a><span data-ttu-id="03d32-394">30110</span><span class="sxs-lookup"><span data-stu-id="03d32-394">30110</span></span>
<span data-ttu-id="03d32-395">このテナントの学生情報サービスが登録されていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-395">Student Information Services has not been registered for this tenant.</span></span>

### <a name="30111"></a><span data-ttu-id="03d32-396">30111</span><span class="sxs-lookup"><span data-stu-id="03d32-396">30111</span></span>
<span data-ttu-id="03d32-397">学生情報サービスに一般的なエラーがあります。</span><span class="sxs-lookup"><span data-stu-id="03d32-397">There is a generic error with Student Information Services.</span></span>

### <a name="30112"></a><span data-ttu-id="03d32-398">30112</span><span class="sxs-lookup"><span data-stu-id="03d32-398">30112</span></span>
<span data-ttu-id="03d32-399">要求によって影響を受けた複数のユーザーは、同じユーザー名でした。</span><span class="sxs-lookup"><span data-stu-id="03d32-399">Multiple users affected by the request had the same username.</span></span>

### <a name="30113"></a><span data-ttu-id="03d32-400">30113</span><span class="sxs-lookup"><span data-stu-id="03d32-400">30113</span></span>
<span data-ttu-id="03d32-401">ノートブックは、招待を許可するように構成されていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-401">The notebook is not configured to allow invites.</span></span>

### <a name="30114"></a><span data-ttu-id="03d32-402">30114</span><span class="sxs-lookup"><span data-stu-id="03d32-402">30114</span></span>
<span data-ttu-id="03d32-403">必須パラメーターがありません。</span><span class="sxs-lookup"><span data-stu-id="03d32-403">There is a required parameter missing.</span></span>

## <a name="codes-from-40001-to-49999"></a><span data-ttu-id="03d32-404">40001 から 49999 のコード</span><span class="sxs-lookup"><span data-stu-id="03d32-404">Codes from 40001 to 49999</span></span>
<span data-ttu-id="03d32-405">ユーザーまたはアプリケーションに、適切なアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="03d32-405">The user or application does not have the correct permissions.</span></span>

### <a name="40001"></a><span data-ttu-id="03d32-406">40001</span><span class="sxs-lookup"><span data-stu-id="03d32-406">40001</span></span>
<span data-ttu-id="03d32-407">要求に、有効な OAuth トークンが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-407">The request doesn't contain a valid OAuth token.</span></span> <span data-ttu-id="03d32-408">「[メモのアクセス許可](permissions_reference.md#notes-permissions)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-408">See [Notes permissions](permissions_reference.md#notes-permissions).</span></span>

### <a name="40002"></a><span data-ttu-id="03d32-409">40002</span><span class="sxs-lookup"><span data-stu-id="03d32-409">40002</span></span>
<span data-ttu-id="03d32-410">ユーザーは、要求された場所に書き込むアクセス許可を持っていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-410">The user doesn't have permission to write to the requested location.</span></span>

### <a name="40003"></a><span data-ttu-id="03d32-411">40003</span><span class="sxs-lookup"><span data-stu-id="03d32-411">40003</span></span>
<span data-ttu-id="03d32-412">ユーザーは、要求されたリソースにアクセスする許可を持っていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-412">The user doesn't have permission to access the requested resource.</span></span>

### <a name="40004"></a><span data-ttu-id="03d32-413">40004</span><span class="sxs-lookup"><span data-stu-id="03d32-413">40004</span></span>
<span data-ttu-id="03d32-414">OAuth トークンには、要求されたアクションを実行するために必要なスコープが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-414">The OAuth token doesn't have the required scopes to perform the requested action.</span></span> <span data-ttu-id="03d32-415">「[メモのアクセス許可](permissions_reference.md#notes-permissions)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-415">See [Notes permissions](permissions_reference.md#notes-permissions).</span></span>

### <a name="40006"></a><span data-ttu-id="03d32-416">40006</span><span class="sxs-lookup"><span data-stu-id="03d32-416">40006</span></span> 
<span data-ttu-id="03d32-417">OAuth トークンには、要求されたアクションを実行するために必要なスコープが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="03d32-417">The OAuth token doesn't have the required scopes to perform the requested action.</span></span> <span data-ttu-id="03d32-418">具体的には、編集のアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="03d32-418">Specifically the edit permission.</span></span> <span data-ttu-id="03d32-419">「[メモのアクセス許可](permissions_reference.md#notes-permissions)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03d32-419">See [Notes permissions](permissions_reference.md#notes-permissions).</span></span>

### <a name="40007"></a><span data-ttu-id="03d32-420">40007</span><span class="sxs-lookup"><span data-stu-id="03d32-420">40007</span></span>
<span data-ttu-id="03d32-421">ユーザーには、このリソースにアクセスする権限がありません。</span><span class="sxs-lookup"><span data-stu-id="03d32-421">The current user does not have sufficient permissions to perform this action.</span></span>

### <a name="40008"></a><span data-ttu-id="03d32-422">40008</span><span class="sxs-lookup"><span data-stu-id="03d32-422">40008</span></span>
<span data-ttu-id="03d32-423">このリソースへのアクセスが禁止されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-423">Access is Forbidden for this resource.</span></span>

### <a name="40009"></a><span data-ttu-id="03d32-424">40009</span><span class="sxs-lookup"><span data-stu-id="03d32-424">40009</span></span>
<span data-ttu-id="03d32-425">コンテナーは、既に別のリソースに使用されています。</span><span class="sxs-lookup"><span data-stu-id="03d32-425">The container is already in use by another resource.</span></span>

## <a name="see-also"></a><span data-ttu-id="03d32-426">関連項目</span><span class="sxs-lookup"><span data-stu-id="03d32-426">See also</span></span>

- [<span data-ttu-id="03d32-427">Microsoft Graph のエラー応答とリソースの種類</span><span class="sxs-lookup"><span data-stu-id="03d32-427">Microsoft Graph error responses and resource types</span></span>](errors.md)
- [<span data-ttu-id="03d32-428">OneNote の参照</span><span class="sxs-lookup"><span data-stu-id="03d32-428">OneNote JavaScript API reference</span></span>](../api-reference/v1.0/resources/onenote.md)
