# <a name="create-windowsmobilemsi"></a><span data-ttu-id="d95b5-101">Create windowsMobileMSI</span><span class="sxs-lookup"><span data-stu-id="d95b5-101">Create windowsMobileMSI</span></span>

> <span data-ttu-id="d95b5-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d95b5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d95b5-103">新しく [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d95b5-103">Create a new [plannerBucket](../resources/intune_apps_windowsmobilemsi.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d95b5-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="d95b5-104">Prerequisites</span></span>
<span data-ttu-id="d95b5-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d95b5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d95b5-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="d95b5-107">Permission type</span></span>|<span data-ttu-id="d95b5-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="d95b5-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d95b5-109">委任 (職場または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="d95b5-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d95b5-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d95b5-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d95b5-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="d95b5-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d95b5-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d95b5-112">Not supported.</span></span>|
|<span data-ttu-id="d95b5-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d95b5-113">Application</span></span>|<span data-ttu-id="d95b5-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d95b5-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d95b5-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="d95b5-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="d95b5-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d95b5-116">Request headers</span></span>
|<span data-ttu-id="d95b5-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d95b5-117">Header</span></span>|<span data-ttu-id="d95b5-118">値</span><span class="sxs-lookup"><span data-stu-id="d95b5-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d95b5-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d95b5-119">Authorization</span></span>|<span data-ttu-id="d95b5-120">ベアラー &lt;トークン&gt; が必須。</span><span class="sxs-lookup"><span data-stu-id="d95b5-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="d95b5-121">Accept</span><span class="sxs-lookup"><span data-stu-id="d95b5-121">Accept</span></span>|<span data-ttu-id="d95b5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d95b5-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d95b5-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="d95b5-123">Request body</span></span>
<span data-ttu-id="d95b5-124">要求本文で、windowsMobileMSI オブジェクト用の JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="d95b5-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="d95b5-125">次の表に、windowsMobileMSI 作成時に必要となるプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="d95b5-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="d95b5-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d95b5-126">Property</span></span>|<span data-ttu-id="d95b5-127">型</span><span class="sxs-lookup"><span data-stu-id="d95b5-127">Type</span></span>|<span data-ttu-id="d95b5-128">説明</span><span class="sxs-lookup"><span data-stu-id="d95b5-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d95b5-129">id</span><span class="sxs-lookup"><span data-stu-id="d95b5-129">id</span></span>|<span data-ttu-id="d95b5-130">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-130">String</span></span>|<span data-ttu-id="d95b5-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="d95b5-131">Name of the entity.</span></span> <span data-ttu-id="d95b5-132">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-133">displayName</span><span class="sxs-lookup"><span data-stu-id="d95b5-133">displayName</span></span>|<span data-ttu-id="d95b5-134">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-134">String</span></span>|<span data-ttu-id="d95b5-135">管理者が提供またはインポートしたアプリのタイトル。</span><span class="sxs-lookup"><span data-stu-id="d95b5-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="d95b5-136">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-137">description</span><span class="sxs-lookup"><span data-stu-id="d95b5-137">description</span></span>|<span data-ttu-id="d95b5-138">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-138">String</span></span>|<span data-ttu-id="d95b5-139">アプリの説明。</span><span class="sxs-lookup"><span data-stu-id="d95b5-139">The description of the app.</span></span> <span data-ttu-id="d95b5-140">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-141">publisher</span><span class="sxs-lookup"><span data-stu-id="d95b5-141">Publisher</span></span>|<span data-ttu-id="d95b5-142">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-142">String</span></span>|<span data-ttu-id="d95b5-143">アプリの発行元。</span><span class="sxs-lookup"><span data-stu-id="d95b5-143">The name of the app.</span></span> <span data-ttu-id="d95b5-144">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="d95b5-145">largeIcon</span></span>|[<span data-ttu-id="d95b5-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="d95b5-146">MimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="d95b5-147">アプリの詳細に表示され、アイコンのアップロードに使用される大きなアイコン。</span><span class="sxs-lookup"><span data-stu-id="d95b5-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="d95b5-148">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d95b5-149">createdDateTime</span></span>|<span data-ttu-id="d95b5-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d95b5-150">DateTimeOffset</span></span>|<span data-ttu-id="d95b5-151">アプリが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="d95b5-151">The date and time when the page was created.</span></span> <span data-ttu-id="d95b5-152">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d95b5-153">lastModifiedDateTime</span></span>|<span data-ttu-id="d95b5-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d95b5-154">DateTimeOffset</span></span>|<span data-ttu-id="d95b5-155">アプリが最後に変更された日時。</span><span class="sxs-lookup"><span data-stu-id="d95b5-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="d95b5-156">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="d95b5-157">isFeatured</span></span>|<span data-ttu-id="d95b5-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="d95b5-158">Boolean</span></span>|<span data-ttu-id="d95b5-159">アプリが管理者のおすすめとしてマークされたかどうかを示す値。[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="d95b5-160">privacyInformationUrl</span></span>|<span data-ttu-id="d95b5-161">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-161">String</span></span>|<span data-ttu-id="d95b5-162">プライバシーに関する声明の URL。</span><span class="sxs-lookup"><span data-stu-id="d95b5-162">The privacy statement Url.</span></span> <span data-ttu-id="d95b5-163">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="d95b5-164">informationUrl</span></span>|<span data-ttu-id="d95b5-165">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-165">String</span></span>|<span data-ttu-id="d95b5-166">詳細情報の URL。</span><span class="sxs-lookup"><span data-stu-id="d95b5-166">The more information Url.</span></span> <span data-ttu-id="d95b5-167">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-168">owner</span><span class="sxs-lookup"><span data-stu-id="d95b5-168">owner</span></span>|<span data-ttu-id="d95b5-169">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-169">String</span></span>|<span data-ttu-id="d95b5-170">アプリの所有者。</span><span class="sxs-lookup"><span data-stu-id="d95b5-170">The owner of the timesheet.</span></span> <span data-ttu-id="d95b5-171">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-172">developer</span><span class="sxs-lookup"><span data-stu-id="d95b5-172">developer</span></span>|<span data-ttu-id="d95b5-173">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-173">String</span></span>|<span data-ttu-id="d95b5-174">アプリの開発者。</span><span class="sxs-lookup"><span data-stu-id="d95b5-174">The name of the app.</span></span> <span data-ttu-id="d95b5-175">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-176">notes</span><span class="sxs-lookup"><span data-stu-id="d95b5-176">notes</span></span>|<span data-ttu-id="d95b5-177">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-177">String</span></span>|<span data-ttu-id="d95b5-178">アプリ用のメモ。</span><span class="sxs-lookup"><span data-stu-id="d95b5-178">Notes for the app.</span></span> <span data-ttu-id="d95b5-179">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="d95b5-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="d95b5-180">publishingState</span></span>|<span data-ttu-id="d95b5-181">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-181">String</span></span>|<span data-ttu-id="d95b5-182">アプリの発行の状態。</span><span class="sxs-lookup"><span data-stu-id="d95b5-182">The publishing state for the app.</span></span> <span data-ttu-id="d95b5-183">アプリが発行されていない限り、アプリを割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="d95b5-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="d95b5-184">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します。可能な値は、`notPublished`、`processing`、`published` です。</span><span class="sxs-lookup"><span data-stu-id="d95b5-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="d95b5-185">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="d95b5-185">committedContentVersion</span></span>|<span data-ttu-id="d95b5-186">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-186">String</span></span>|<span data-ttu-id="d95b5-187">内部にコミットされたコンテンツのバージョン。</span><span class="sxs-lookup"><span data-stu-id="d95b5-187">The internal committed content version.</span></span> <span data-ttu-id="d95b5-188">[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-188">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="d95b5-189">fileName</span><span class="sxs-lookup"><span data-stu-id="d95b5-189">FileName</span></span>|<span data-ttu-id="d95b5-190">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-190">String</span></span>|<span data-ttu-id="d95b5-191">メインの Lob アプリケーションのファイル名。</span><span class="sxs-lookup"><span data-stu-id="d95b5-191">The name of the main Lob application file.</span></span> <span data-ttu-id="d95b5-192">[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-192">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="d95b5-193">size</span><span class="sxs-lookup"><span data-stu-id="d95b5-193">size</span></span>|<span data-ttu-id="d95b5-194">Int64</span><span class="sxs-lookup"><span data-stu-id="d95b5-194">Int64</span></span>|<span data-ttu-id="d95b5-195">アップロードされたすべてのファイルを含む合計サイズ。</span><span class="sxs-lookup"><span data-stu-id="d95b5-195">The total size, including all uploaded files.</span></span> <span data-ttu-id="d95b5-196">[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d95b5-196">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="d95b5-197">commandLine</span><span class="sxs-lookup"><span data-stu-id="d95b5-197">Command-line:</span></span>|<span data-ttu-id="d95b5-198">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-198">String</span></span>|<span data-ttu-id="d95b5-199">コマンド ライン。</span><span class="sxs-lookup"><span data-stu-id="d95b5-199">The command line.</span></span>|
|<span data-ttu-id="d95b5-200">productCode</span><span class="sxs-lookup"><span data-stu-id="d95b5-200">ProductCode</span></span>|<span data-ttu-id="d95b5-201">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-201">String</span></span>|<span data-ttu-id="d95b5-202">製品コード。</span><span class="sxs-lookup"><span data-stu-id="d95b5-202">The product code.</span></span>|
|<span data-ttu-id="d95b5-203">productVersion</span><span class="sxs-lookup"><span data-stu-id="d95b5-203">productVersion</span></span>|<span data-ttu-id="d95b5-204">String</span><span class="sxs-lookup"><span data-stu-id="d95b5-204">String</span></span>|<span data-ttu-id="d95b5-205">Windows Mobile MSI 基幹業務 (LoB) アプリの製品のバージョン。</span><span class="sxs-lookup"><span data-stu-id="d95b5-205">The product version of Windows Mobile MSI Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="d95b5-206">ignoreVersionDetection</span><span class="sxs-lookup"><span data-stu-id="d95b5-206">ignoreVersionDetection</span></span>|<span data-ttu-id="d95b5-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="d95b5-207">Boolean</span></span>|<span data-ttu-id="d95b5-208">アプリをデバイスにインストールした後に、アプリのバージョンを使用してアプリを検出するかどうかを制御するブール値。</span><span class="sxs-lookup"><span data-stu-id="d95b5-208">A boolean to control whether the app's version will be used to detect the app after it is installed on a device.</span></span> <span data-ttu-id="d95b5-209">自己更新機能を使用する Windows Mobile MSI 基幹業務 (LoB) アプリの場合は、true に設定します。</span><span class="sxs-lookup"><span data-stu-id="d95b5-209">Set this to true for Windows Mobile MSI Line of Business (LoB) apps that use a self update feature.</span></span>|



## <a name="response"></a><span data-ttu-id="d95b5-210">応答</span><span class="sxs-lookup"><span data-stu-id="d95b5-210">Response</span></span>
<span data-ttu-id="d95b5-211">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [windowsMobileMSI](../resources/intune_apps_windowsmobilemsi.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d95b5-211">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_apps_windowsmobilemsi.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d95b5-212">例</span><span class="sxs-lookup"><span data-stu-id="d95b5-212">Example</span></span>
### <a name="request"></a><span data-ttu-id="d95b5-213">要求</span><span class="sxs-lookup"><span data-stu-id="d95b5-213">Request</span></span>
<span data-ttu-id="d95b5-214">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="d95b5-214">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 919

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```

### <a name="response"></a><span data-ttu-id="d95b5-215">応答</span><span class="sxs-lookup"><span data-stu-id="d95b5-215">Response</span></span>
<span data-ttu-id="d95b5-p119">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="d95b5-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1027

{
  "@odata.type": "#microsoft.graph.windowsMobileMSI",
  "id": "aa453e5d-3e5d-aa45-5d3e-45aa5d3e45aa",
  "displayName": "Display Name value",
  "description": "Description value",
  "publisher": "Publisher value",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "Type value",
    "value": "dmFsdWU="
  },
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "isFeatured": true,
  "privacyInformationUrl": "https://example.com/privacyInformationUrl/",
  "informationUrl": "https://example.com/informationUrl/",
  "owner": "Owner value",
  "developer": "Developer value",
  "notes": "Notes value",
  "publishingState": "processing",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "commandLine": "Command Line value",
  "productCode": "Product Code value",
  "productVersion": "Product Version value",
  "ignoreVersionDetection": true
}
```


