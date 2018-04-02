# <a name="create-windowsuniversalappx"></a><span data-ttu-id="5e618-101">Create windowsUniversalAppX</span><span class="sxs-lookup"><span data-stu-id="5e618-101">Create windowsUniversalAppX</span></span>

> <span data-ttu-id="5e618-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e618-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5e618-103">新しい [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e618-103">Create a new [plannerBucket](../resources/intune_apps_windowsuniversalappx.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5e618-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="5e618-104">Prerequisites</span></span>
<span data-ttu-id="5e618-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e618-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5e618-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="5e618-107">Permission type</span></span>|<span data-ttu-id="5e618-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="5e618-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5e618-109">委任 (職場または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="5e618-109">Delegated (work or school account)</span></span>|<span data-ttu-id="5e618-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5e618-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5e618-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="5e618-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5e618-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5e618-112">Not supported.</span></span>|
|<span data-ttu-id="5e618-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="5e618-113">Application</span></span>|<span data-ttu-id="5e618-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="5e618-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5e618-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="5e618-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="5e618-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="5e618-116">Request headers</span></span>
|<span data-ttu-id="5e618-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="5e618-117">Header</span></span>|<span data-ttu-id="5e618-118">値</span><span class="sxs-lookup"><span data-stu-id="5e618-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5e618-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="5e618-119">Authorization</span></span>|<span data-ttu-id="5e618-120">ベアラー &lt;トークン&gt; が必須。</span><span class="sxs-lookup"><span data-stu-id="5e618-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="5e618-121">Accept</span><span class="sxs-lookup"><span data-stu-id="5e618-121">Accept</span></span>|<span data-ttu-id="5e618-122">application/json</span><span class="sxs-lookup"><span data-stu-id="5e618-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5e618-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="5e618-123">Request body</span></span>
<span data-ttu-id="5e618-124">要求本文で、windowsUniversalAppX オブジェクトの JSON 表現を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e618-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="5e618-125">次の表に、windowsUniversalAppX の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="5e618-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="5e618-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="5e618-126">Property</span></span>|<span data-ttu-id="5e618-127">型</span><span class="sxs-lookup"><span data-stu-id="5e618-127">Type</span></span>|<span data-ttu-id="5e618-128">説明</span><span class="sxs-lookup"><span data-stu-id="5e618-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5e618-129">id</span><span class="sxs-lookup"><span data-stu-id="5e618-129">id</span></span>|<span data-ttu-id="5e618-130">String</span><span class="sxs-lookup"><span data-stu-id="5e618-130">String</span></span>|<span data-ttu-id="5e618-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="5e618-131">Name of the entity.</span></span> <span data-ttu-id="5e618-132">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-133">displayName</span><span class="sxs-lookup"><span data-stu-id="5e618-133">displayName</span></span>|<span data-ttu-id="5e618-134">String</span><span class="sxs-lookup"><span data-stu-id="5e618-134">String</span></span>|<span data-ttu-id="5e618-135">管理者が提供またはインポートしたアプリのタイトル。</span><span class="sxs-lookup"><span data-stu-id="5e618-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="5e618-136">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-137">description</span><span class="sxs-lookup"><span data-stu-id="5e618-137">description</span></span>|<span data-ttu-id="5e618-138">String</span><span class="sxs-lookup"><span data-stu-id="5e618-138">String</span></span>|<span data-ttu-id="5e618-139">アプリの説明。</span><span class="sxs-lookup"><span data-stu-id="5e618-139">The description of the app.</span></span> <span data-ttu-id="5e618-140">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-141">publisher</span><span class="sxs-lookup"><span data-stu-id="5e618-141">Publisher</span></span>|<span data-ttu-id="5e618-142">String</span><span class="sxs-lookup"><span data-stu-id="5e618-142">String</span></span>|<span data-ttu-id="5e618-143">アプリの発行元。</span><span class="sxs-lookup"><span data-stu-id="5e618-143">The name of the app.</span></span> <span data-ttu-id="5e618-144">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="5e618-145">largeIcon</span></span>|[<span data-ttu-id="5e618-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="5e618-146">MimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="5e618-147">アプリの詳細に表示され、アイコンのアップロードに使用される大きなアイコン。</span><span class="sxs-lookup"><span data-stu-id="5e618-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="5e618-148">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="5e618-149">createdDateTime</span></span>|<span data-ttu-id="5e618-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e618-150">DateTimeOffset</span></span>|<span data-ttu-id="5e618-151">アプリが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="5e618-151">The date and time when the page was created.</span></span> <span data-ttu-id="5e618-152">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="5e618-153">lastModifiedDateTime</span></span>|<span data-ttu-id="5e618-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5e618-154">DateTimeOffset</span></span>|<span data-ttu-id="5e618-155">アプリが最後に変更された日時。</span><span class="sxs-lookup"><span data-stu-id="5e618-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="5e618-156">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="5e618-157">isFeatured</span></span>|<span data-ttu-id="5e618-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="5e618-158">Boolean</span></span>|<span data-ttu-id="5e618-159">アプリが管理者のおすすめとしてマークされたかどうかを示す値。[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="5e618-160">privacyInformationUrl</span></span>|<span data-ttu-id="5e618-161">String</span><span class="sxs-lookup"><span data-stu-id="5e618-161">String</span></span>|<span data-ttu-id="5e618-162">プライバシーに関する声明の URL。</span><span class="sxs-lookup"><span data-stu-id="5e618-162">The privacy statement Url.</span></span> <span data-ttu-id="5e618-163">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="5e618-164">informationUrl</span></span>|<span data-ttu-id="5e618-165">String</span><span class="sxs-lookup"><span data-stu-id="5e618-165">String</span></span>|<span data-ttu-id="5e618-166">詳細情報の URL。</span><span class="sxs-lookup"><span data-stu-id="5e618-166">The more information Url.</span></span> <span data-ttu-id="5e618-167">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-168">owner</span><span class="sxs-lookup"><span data-stu-id="5e618-168">owner</span></span>|<span data-ttu-id="5e618-169">String</span><span class="sxs-lookup"><span data-stu-id="5e618-169">String</span></span>|<span data-ttu-id="5e618-170">アプリの所有者。</span><span class="sxs-lookup"><span data-stu-id="5e618-170">The owner of the timesheet.</span></span> <span data-ttu-id="5e618-171">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-172">developer</span><span class="sxs-lookup"><span data-stu-id="5e618-172">developer</span></span>|<span data-ttu-id="5e618-173">String</span><span class="sxs-lookup"><span data-stu-id="5e618-173">String</span></span>|<span data-ttu-id="5e618-174">アプリの開発者。</span><span class="sxs-lookup"><span data-stu-id="5e618-174">The name of the app.</span></span> <span data-ttu-id="5e618-175">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-176">notes</span><span class="sxs-lookup"><span data-stu-id="5e618-176">notes</span></span>|<span data-ttu-id="5e618-177">String</span><span class="sxs-lookup"><span data-stu-id="5e618-177">String</span></span>|<span data-ttu-id="5e618-178">アプリ用のメモ。</span><span class="sxs-lookup"><span data-stu-id="5e618-178">Notes for the app.</span></span> <span data-ttu-id="5e618-179">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="5e618-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="5e618-180">publishingState</span></span>|<span data-ttu-id="5e618-181">String</span><span class="sxs-lookup"><span data-stu-id="5e618-181">String</span></span>|<span data-ttu-id="5e618-182">アプリの発行の状態。</span><span class="sxs-lookup"><span data-stu-id="5e618-182">The publishing state for the app.</span></span> <span data-ttu-id="5e618-183">アプリが発行されていない限り、アプリを割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="5e618-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="5e618-184">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します。可能な値は、`notPublished`、`processing`、`published` です。</span><span class="sxs-lookup"><span data-stu-id="5e618-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="5e618-185">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="5e618-185">committedContentVersion</span></span>|<span data-ttu-id="5e618-186">String</span><span class="sxs-lookup"><span data-stu-id="5e618-186">String</span></span>|<span data-ttu-id="5e618-187">内部にコミットされたコンテンツのバージョン。</span><span class="sxs-lookup"><span data-stu-id="5e618-187">The internal committed content version.</span></span> <span data-ttu-id="5e618-188">[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-188">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="5e618-189">fileName</span><span class="sxs-lookup"><span data-stu-id="5e618-189">FileName</span></span>|<span data-ttu-id="5e618-190">String</span><span class="sxs-lookup"><span data-stu-id="5e618-190">String</span></span>|<span data-ttu-id="5e618-191">メインの Lob アプリケーションのファイル名。</span><span class="sxs-lookup"><span data-stu-id="5e618-191">The name of the main Lob application file.</span></span> <span data-ttu-id="5e618-192">[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-192">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="5e618-193">size</span><span class="sxs-lookup"><span data-stu-id="5e618-193">size</span></span>|<span data-ttu-id="5e618-194">Int64</span><span class="sxs-lookup"><span data-stu-id="5e618-194">Int64</span></span>|<span data-ttu-id="5e618-195">アップロードされたすべてのファイルを含む合計サイズ。</span><span class="sxs-lookup"><span data-stu-id="5e618-195">The total size, including all uploaded files.</span></span> <span data-ttu-id="5e618-196">[mobileLobApp](../resources/intune_apps_mobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="5e618-196">Inherited from [mobileLobApp](../resources/intune_apps_mobilelobapp.md)</span></span>|
|<span data-ttu-id="5e618-197">applicableArchitectures</span><span class="sxs-lookup"><span data-stu-id="5e618-197">applicableArchitectures</span></span>|<span data-ttu-id="5e618-198">String</span><span class="sxs-lookup"><span data-stu-id="5e618-198">String</span></span>|<span data-ttu-id="5e618-199">このアプリを実行できる Windows アーキテクチャ。</span><span class="sxs-lookup"><span data-stu-id="5e618-199">The Windows architecture(s) for which this app can run on.</span></span> <span data-ttu-id="5e618-200">可能な値は、`none`、`x86`、`x64`、`arm`、`neutral` です。</span><span class="sxs-lookup"><span data-stu-id="5e618-200">Possible values are: `none`, `x86`, `x64`, `arm`, `neutral`.</span></span>|
|<span data-ttu-id="5e618-201">applicableDeviceTypes</span><span class="sxs-lookup"><span data-stu-id="5e618-201">applicableDeviceTypes</span></span>|<span data-ttu-id="5e618-202">String</span><span class="sxs-lookup"><span data-stu-id="5e618-202">String</span></span>|<span data-ttu-id="5e618-203">このアプリを実行できる Windows デバイスの種類。</span><span class="sxs-lookup"><span data-stu-id="5e618-203">The Windows device type(s) for which this app can run on.</span></span> <span data-ttu-id="5e618-204">可能な値は、`none`、`desktop`、`mobile`、`holographic`、`team` です。</span><span class="sxs-lookup"><span data-stu-id="5e618-204">Possible values are: `none`, `desktop`, `mobile`, `holographic`, `team`.</span></span>|
|<span data-ttu-id="5e618-205">identityName</span><span class="sxs-lookup"><span data-stu-id="5e618-205">identityName</span></span>|<span data-ttu-id="5e618-206">String</span><span class="sxs-lookup"><span data-stu-id="5e618-206">String</span></span>|<span data-ttu-id="5e618-207">ID 名。</span><span class="sxs-lookup"><span data-stu-id="5e618-207">The Identity Name.</span></span>|
|<span data-ttu-id="5e618-208">identityPublisherHash</span><span class="sxs-lookup"><span data-stu-id="5e618-208">identityPublisherHash</span></span>|<span data-ttu-id="5e618-209">String</span><span class="sxs-lookup"><span data-stu-id="5e618-209">String</span></span>|<span data-ttu-id="5e618-210">ID の発行元のハッシュ。</span><span class="sxs-lookup"><span data-stu-id="5e618-210">The Identity Publisher Hash.</span></span>|
|<span data-ttu-id="5e618-211">identityResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="5e618-211">identityResourceIdentifier</span></span>|<span data-ttu-id="5e618-212">String</span><span class="sxs-lookup"><span data-stu-id="5e618-212">String</span></span>|<span data-ttu-id="5e618-213">ID のリソースの識別子。</span><span class="sxs-lookup"><span data-stu-id="5e618-213">The Identity Resource Identifier.</span></span>|
|<span data-ttu-id="5e618-214">isBundle</span><span class="sxs-lookup"><span data-stu-id="5e618-214">isBundle</span></span>|<span data-ttu-id="5e618-215">Boolean</span><span class="sxs-lookup"><span data-stu-id="5e618-215">Boolean</span></span>|<span data-ttu-id="5e618-216">アプリがバンドルかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5e618-216">Whether or not the app is a bundle.</span></span>|
|<span data-ttu-id="5e618-217">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5e618-217">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="5e618-218">windowsMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5e618-218">windowsMinimumOperatingSystem</span></span>](../resources/intune_apps_windowsminimumoperatingsystem.md)|<span data-ttu-id="5e618-219">該当するオペレーティング システムの最小の値です。</span><span class="sxs-lookup"><span data-stu-id="5e618-219">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="5e618-220">identityVersion</span><span class="sxs-lookup"><span data-stu-id="5e618-220">identityVersion</span></span>|<span data-ttu-id="5e618-221">String</span><span class="sxs-lookup"><span data-stu-id="5e618-221">String</span></span>|<span data-ttu-id="5e618-222">ID のバージョン。</span><span class="sxs-lookup"><span data-stu-id="5e618-222">The identity version.</span></span>|



## <a name="response"></a><span data-ttu-id="5e618-223">応答</span><span class="sxs-lookup"><span data-stu-id="5e618-223">Response</span></span>
<span data-ttu-id="5e618-224">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [windowsUniversalAppX](../resources/intune_apps_windowsuniversalappx.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="5e618-224">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_windowsuniversalappx.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5e618-225">例</span><span class="sxs-lookup"><span data-stu-id="5e618-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="5e618-226">要求</span><span class="sxs-lookup"><span data-stu-id="5e618-226">Request</span></span>
<span data-ttu-id="5e618-227">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="5e618-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1253

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
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
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "Identity Version value"
}
```

### <a name="response"></a><span data-ttu-id="5e618-228">応答</span><span class="sxs-lookup"><span data-stu-id="5e618-228">Response</span></span>
<span data-ttu-id="5e618-p120">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="5e618-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1361

{
  "@odata.type": "#microsoft.graph.windowsUniversalAppX",
  "id": "4bc47eba-7eba-4bc4-ba7e-c44bba7ec44b",
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
  "applicableArchitectures": "x86",
  "applicableDeviceTypes": "desktop",
  "identityName": "Identity Name value",
  "identityPublisherHash": "Identity Publisher Hash value",
  "identityResourceIdentifier": "Identity Resource Identifier value",
  "isBundle": true,
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem",
    "v8_0": true,
    "v8_1": true,
    "v10_0": true
  },
  "identityVersion": "Identity Version value"
}
```


