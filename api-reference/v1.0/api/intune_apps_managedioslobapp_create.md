# <a name="create-managedioslobapp"></a><span data-ttu-id="8db78-101">Create managedIOSLobApp</span><span class="sxs-lookup"><span data-stu-id="8db78-101">Create managedIOSLobApp</span></span>

> <span data-ttu-id="8db78-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8db78-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8db78-103">新しい [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8db78-103">Create a new [plannerBucket](../resources/intune_apps_managedioslobapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8db78-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="8db78-104">Prerequisites</span></span>
<span data-ttu-id="8db78-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8db78-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8db78-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="8db78-107">Permission type</span></span>|<span data-ttu-id="8db78-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="8db78-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8db78-109">委任 (職場または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="8db78-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8db78-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8db78-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="8db78-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="8db78-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8db78-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8db78-112">Not supported.</span></span>|
|<span data-ttu-id="8db78-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="8db78-113">Application</span></span>|<span data-ttu-id="8db78-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8db78-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8db78-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="8db78-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps
```

## <a name="request-headers"></a><span data-ttu-id="8db78-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="8db78-116">Request headers</span></span>
|<span data-ttu-id="8db78-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="8db78-117">Header</span></span>|<span data-ttu-id="8db78-118">値</span><span class="sxs-lookup"><span data-stu-id="8db78-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8db78-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8db78-119">Authorization</span></span>|<span data-ttu-id="8db78-120">ベアラー &lt;トークン&gt; が必須。</span><span class="sxs-lookup"><span data-stu-id="8db78-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="8db78-121">Accept</span><span class="sxs-lookup"><span data-stu-id="8db78-121">Accept</span></span>|<span data-ttu-id="8db78-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8db78-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8db78-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="8db78-123">Request body</span></span>
<span data-ttu-id="8db78-124">要求本文で、managedIOSLobApp オブジェクト用の JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="8db78-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="8db78-125">次の表に、managedDeviceOverview の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="8db78-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="8db78-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8db78-126">Property</span></span>|<span data-ttu-id="8db78-127">型</span><span class="sxs-lookup"><span data-stu-id="8db78-127">Type</span></span>|<span data-ttu-id="8db78-128">説明</span><span class="sxs-lookup"><span data-stu-id="8db78-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8db78-129">id</span><span class="sxs-lookup"><span data-stu-id="8db78-129">id</span></span>|<span data-ttu-id="8db78-130">String</span><span class="sxs-lookup"><span data-stu-id="8db78-130">String</span></span>|<span data-ttu-id="8db78-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="8db78-131">Name of the entity.</span></span> <span data-ttu-id="8db78-132">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-133">displayName</span><span class="sxs-lookup"><span data-stu-id="8db78-133">displayName</span></span>|<span data-ttu-id="8db78-134">String</span><span class="sxs-lookup"><span data-stu-id="8db78-134">String</span></span>|<span data-ttu-id="8db78-135">管理者が提供またはインポートしたアプリのタイトル。</span><span class="sxs-lookup"><span data-stu-id="8db78-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="8db78-136">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-137">description</span><span class="sxs-lookup"><span data-stu-id="8db78-137">description</span></span>|<span data-ttu-id="8db78-138">String</span><span class="sxs-lookup"><span data-stu-id="8db78-138">String</span></span>|<span data-ttu-id="8db78-139">アプリの説明。</span><span class="sxs-lookup"><span data-stu-id="8db78-139">The description of the app.</span></span> <span data-ttu-id="8db78-140">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-141">publisher</span><span class="sxs-lookup"><span data-stu-id="8db78-141">Publisher</span></span>|<span data-ttu-id="8db78-142">String</span><span class="sxs-lookup"><span data-stu-id="8db78-142">String</span></span>|<span data-ttu-id="8db78-143">アプリの発行元。</span><span class="sxs-lookup"><span data-stu-id="8db78-143">The name of the app.</span></span> <span data-ttu-id="8db78-144">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="8db78-145">largeIcon</span></span>|[<span data-ttu-id="8db78-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="8db78-146">MimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="8db78-147">アプリの詳細に表示され、アイコンのアップロードに使用される大きなアイコン。</span><span class="sxs-lookup"><span data-stu-id="8db78-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="8db78-148">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8db78-149">createdDateTime</span></span>|<span data-ttu-id="8db78-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8db78-150">DateTimeOffset</span></span>|<span data-ttu-id="8db78-151">アプリが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="8db78-151">The date and time when the page was created.</span></span> <span data-ttu-id="8db78-152">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8db78-153">lastModifiedDateTime</span></span>|<span data-ttu-id="8db78-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8db78-154">DateTimeOffset</span></span>|<span data-ttu-id="8db78-155">アプリが最後に変更された日時。</span><span class="sxs-lookup"><span data-stu-id="8db78-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="8db78-156">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="8db78-157">isFeatured</span></span>|<span data-ttu-id="8db78-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="8db78-158">Boolean</span></span>|<span data-ttu-id="8db78-159">アプリが管理者のおすすめとしてマークされたかどうかを示す値。[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="8db78-160">privacyInformationUrl</span></span>|<span data-ttu-id="8db78-161">String</span><span class="sxs-lookup"><span data-stu-id="8db78-161">String</span></span>|<span data-ttu-id="8db78-162">プライバシーに関する声明の URL。</span><span class="sxs-lookup"><span data-stu-id="8db78-162">The privacy statement Url.</span></span> <span data-ttu-id="8db78-163">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="8db78-164">informationUrl</span></span>|<span data-ttu-id="8db78-165">String</span><span class="sxs-lookup"><span data-stu-id="8db78-165">String</span></span>|<span data-ttu-id="8db78-166">詳細情報の URL。</span><span class="sxs-lookup"><span data-stu-id="8db78-166">The more information Url.</span></span> <span data-ttu-id="8db78-167">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-168">owner</span><span class="sxs-lookup"><span data-stu-id="8db78-168">owner</span></span>|<span data-ttu-id="8db78-169">String</span><span class="sxs-lookup"><span data-stu-id="8db78-169">String</span></span>|<span data-ttu-id="8db78-170">アプリの所有者。</span><span class="sxs-lookup"><span data-stu-id="8db78-170">The owner of the timesheet.</span></span> <span data-ttu-id="8db78-171">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-172">developer</span><span class="sxs-lookup"><span data-stu-id="8db78-172">developer</span></span>|<span data-ttu-id="8db78-173">String</span><span class="sxs-lookup"><span data-stu-id="8db78-173">String</span></span>|<span data-ttu-id="8db78-174">アプリの開発者。</span><span class="sxs-lookup"><span data-stu-id="8db78-174">The name of the app.</span></span> <span data-ttu-id="8db78-175">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-176">notes</span><span class="sxs-lookup"><span data-stu-id="8db78-176">notes</span></span>|<span data-ttu-id="8db78-177">String</span><span class="sxs-lookup"><span data-stu-id="8db78-177">String</span></span>|<span data-ttu-id="8db78-178">アプリ用のメモ。</span><span class="sxs-lookup"><span data-stu-id="8db78-178">Notes for the app.</span></span> <span data-ttu-id="8db78-179">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="8db78-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="8db78-180">publishingState</span></span>|<span data-ttu-id="8db78-181">String</span><span class="sxs-lookup"><span data-stu-id="8db78-181">String</span></span>|<span data-ttu-id="8db78-182">アプリの発行の状態。</span><span class="sxs-lookup"><span data-stu-id="8db78-182">The publishing state for the app.</span></span> <span data-ttu-id="8db78-183">アプリが発行されていない限り、アプリを割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="8db78-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="8db78-184">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します。可能な値は、`notPublished`、`processing`、`published` です。</span><span class="sxs-lookup"><span data-stu-id="8db78-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|
|<span data-ttu-id="8db78-185">appAvailability</span><span class="sxs-lookup"><span data-stu-id="8db78-185">appAvailability</span></span>|<span data-ttu-id="8db78-186">String</span><span class="sxs-lookup"><span data-stu-id="8db78-186">String</span></span>|<span data-ttu-id="8db78-187">アプリケーションの可用性。</span><span class="sxs-lookup"><span data-stu-id="8db78-187">The Application's availability.</span></span> <span data-ttu-id="8db78-188">[managedApp](../resources/intune_apps_managedapp.md) から継承します。可能な値は、`global`、`lineOfBusiness` です。</span><span class="sxs-lookup"><span data-stu-id="8db78-188">Inherited from [managedApp](../resources/intune_apps_managedapp.md) Possible values are: `global`, `lineOfBusiness`.</span></span>|
|<span data-ttu-id="8db78-189">version</span><span class="sxs-lookup"><span data-stu-id="8db78-189">version</span></span>|<span data-ttu-id="8db78-190">String</span><span class="sxs-lookup"><span data-stu-id="8db78-190">String</span></span>|<span data-ttu-id="8db78-191">アプリケーションのバージョン。</span><span class="sxs-lookup"><span data-stu-id="8db78-191">The Application's version.</span></span> <span data-ttu-id="8db78-192">[managedApp](../resources/intune_apps_managedapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-192">Inherited from [managedApp](../resources/intune_apps_managedapp.md)</span></span>|
|<span data-ttu-id="8db78-193">committedContentVersion</span><span class="sxs-lookup"><span data-stu-id="8db78-193">committedContentVersion</span></span>|<span data-ttu-id="8db78-194">String</span><span class="sxs-lookup"><span data-stu-id="8db78-194">String</span></span>|<span data-ttu-id="8db78-195">内部にコミットされたコンテンツのバージョン。</span><span class="sxs-lookup"><span data-stu-id="8db78-195">The internal committed content version.</span></span> <span data-ttu-id="8db78-196">[managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-196">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="8db78-197">fileName</span><span class="sxs-lookup"><span data-stu-id="8db78-197">FileName</span></span>|<span data-ttu-id="8db78-198">String</span><span class="sxs-lookup"><span data-stu-id="8db78-198">String</span></span>|<span data-ttu-id="8db78-199">メインの Lob アプリケーションのファイル名。</span><span class="sxs-lookup"><span data-stu-id="8db78-199">The name of the main Lob application file.</span></span> <span data-ttu-id="8db78-200">[managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-200">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="8db78-201">size</span><span class="sxs-lookup"><span data-stu-id="8db78-201">size</span></span>|<span data-ttu-id="8db78-202">Int64</span><span class="sxs-lookup"><span data-stu-id="8db78-202">Int64</span></span>|<span data-ttu-id="8db78-203">アップロードされたすべてのファイルを含む合計サイズ。</span><span class="sxs-lookup"><span data-stu-id="8db78-203">The total size, including all uploaded files.</span></span> <span data-ttu-id="8db78-204">[managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="8db78-204">Inherited from [managedMobileLobApp](../resources/intune_apps_managedmobilelobapp.md)</span></span>|
|<span data-ttu-id="8db78-205">bundleId</span><span class="sxs-lookup"><span data-stu-id="8db78-205">bundleId</span></span>|<span data-ttu-id="8db78-206">String</span><span class="sxs-lookup"><span data-stu-id="8db78-206">String</span></span>|<span data-ttu-id="8db78-207">ID 名。</span><span class="sxs-lookup"><span data-stu-id="8db78-207">The Identity Name.</span></span>|
|<span data-ttu-id="8db78-208">applicableDeviceType</span><span class="sxs-lookup"><span data-stu-id="8db78-208">applicableDeviceType</span></span>|[<span data-ttu-id="8db78-209">iosDeviceType</span><span class="sxs-lookup"><span data-stu-id="8db78-209">iosDeviceType</span></span>](../resources/intune_apps_iosdevicetype.md)|<span data-ttu-id="8db78-210">このアプリを実行できる iOS アーキテクチャ。</span><span class="sxs-lookup"><span data-stu-id="8db78-210">The iOS architecture for which this app can run on.</span></span>|
|<span data-ttu-id="8db78-211">minimumSupportedOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8db78-211">minimumSupportedOperatingSystem</span></span>|[<span data-ttu-id="8db78-212">iosMinimumOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8db78-212">iosMinimumOperatingSystem</span></span>](../resources/intune_apps_iosminimumoperatingsystem.md)|<span data-ttu-id="8db78-213">該当するオペレーティング システムの最小の値です。</span><span class="sxs-lookup"><span data-stu-id="8db78-213">The value for the minimum applicable operating system.</span></span>|
|<span data-ttu-id="8db78-214">expirationDateTime</span><span class="sxs-lookup"><span data-stu-id="8db78-214">expirationDateTime</span></span>|<span data-ttu-id="8db78-215">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8db78-215">DateTimeOffset</span></span>|<span data-ttu-id="8db78-216">有効期限。</span><span class="sxs-lookup"><span data-stu-id="8db78-216">: The expiration time for the subscription.</span></span>|
|<span data-ttu-id="8db78-217">VersionNumber</span><span class="sxs-lookup"><span data-stu-id="8db78-217">versionNumber</span></span>|<span data-ttu-id="8db78-218">String</span><span class="sxs-lookup"><span data-stu-id="8db78-218">String</span></span>|<span data-ttu-id="8db78-219">管理対象 iOS 基幹業務 (LoB) アプリのバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="8db78-219">The version number of managed iOS Line of Business (LoB) app.</span></span>|
|<span data-ttu-id="8db78-220">buildNumber</span><span class="sxs-lookup"><span data-stu-id="8db78-220">buildNumber</span></span>|<span data-ttu-id="8db78-221">String</span><span class="sxs-lookup"><span data-stu-id="8db78-221">String</span></span>|<span data-ttu-id="8db78-222">管理対象 iOS 基幹業務 (LoB) アプリのビルド番号。</span><span class="sxs-lookup"><span data-stu-id="8db78-222">The build number of managed iOS Line of Business (LoB) app.</span></span>|



## <a name="response"></a><span data-ttu-id="8db78-223">応答</span><span class="sxs-lookup"><span data-stu-id="8db78-223">Response</span></span>
<span data-ttu-id="8db78-224">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [managedIOSLobApp](../resources/intune_apps_managedioslobapp.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="8db78-224">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_apps_managedioslobapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8db78-225">例</span><span class="sxs-lookup"><span data-stu-id="8db78-225">Example</span></span>
### <a name="request"></a><span data-ttu-id="8db78-226">要求</span><span class="sxs-lookup"><span data-stu-id="8db78-226">Request</span></span>
<span data-ttu-id="8db78-227">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="8db78-227">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps
Content-type: application/json
Content-length: 1331

{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "bundleId": "Bundle Id value",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```

### <a name="response"></a><span data-ttu-id="8db78-228">応答</span><span class="sxs-lookup"><span data-stu-id="8db78-228">Response</span></span>
<span data-ttu-id="8db78-p120">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="8db78-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1439

{
  "@odata.type": "#microsoft.graph.managedIOSLobApp",
  "id": "8f59792d-792d-8f59-2d79-598f2d79598f",
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
  "appAvailability": "lineOfBusiness",
  "version": "Version value",
  "committedContentVersion": "Committed Content Version value",
  "fileName": "File Name value",
  "size": 4,
  "bundleId": "Bundle Id value",
  "applicableDeviceType": {
    "@odata.type": "microsoft.graph.iosDeviceType",
    "iPad": true,
    "iPhoneAndIPod": true
  },
  "minimumSupportedOperatingSystem": {
    "@odata.type": "microsoft.graph.iosMinimumOperatingSystem",
    "v8_0": true,
    "v9_0": true,
    "v10_0": true,
    "v11_0": true
  },
  "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
  "versionNumber": "Version Number value",
  "buildNumber": "Build Number value"
}
```


