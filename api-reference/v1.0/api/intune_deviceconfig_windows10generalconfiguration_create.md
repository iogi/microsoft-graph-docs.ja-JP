# <a name="create-windows10generalconfiguration"></a><span data-ttu-id="b8af8-101">Create windows10GeneralConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8af8-101">Create windows10GeneralConfiguration</span></span>

> <span data-ttu-id="b8af8-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b8af8-103">新しい [windows10GeneralConfiguration](../resources/intune_deviceconfig_windows10generalconfiguration.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-103">Create a new [plannerBucket](../resources/intune_deviceconfig_windows10generalconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b8af8-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="b8af8-104">Prerequisites</span></span>
<span data-ttu-id="b8af8-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b8af8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b8af8-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="b8af8-107">Permission type</span></span>|<span data-ttu-id="b8af8-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="b8af8-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b8af8-109">委任 (職場または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="b8af8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b8af8-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b8af8-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b8af8-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="b8af8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b8af8-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b8af8-112">Not supported.</span></span>|
|<span data-ttu-id="b8af8-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="b8af8-113">Application</span></span>|<span data-ttu-id="b8af8-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="b8af8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b8af8-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="b8af8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="b8af8-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b8af8-116">Request headers</span></span>
|<span data-ttu-id="b8af8-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b8af8-117">Header</span></span>|<span data-ttu-id="b8af8-118">値</span><span class="sxs-lookup"><span data-stu-id="b8af8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b8af8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8af8-119">Authorization</span></span>|<span data-ttu-id="b8af8-120">ベアラー &lt;トークン&gt; が必須。</span><span class="sxs-lookup"><span data-stu-id="b8af8-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="b8af8-121">Accept</span><span class="sxs-lookup"><span data-stu-id="b8af8-121">Accept</span></span>|<span data-ttu-id="b8af8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="b8af8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b8af8-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="b8af8-123">Request body</span></span>
<span data-ttu-id="b8af8-124">要求本文で、windows10GeneralConfiguration オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="b8af8-125">次の表に、windows10GeneralConfiguration の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="b8af8-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="b8af8-126">Property</span></span>|<span data-ttu-id="b8af8-127">型</span><span class="sxs-lookup"><span data-stu-id="b8af8-127">Type</span></span>|<span data-ttu-id="b8af8-128">説明</span><span class="sxs-lookup"><span data-stu-id="b8af8-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b8af8-129">id</span><span class="sxs-lookup"><span data-stu-id="b8af8-129">id</span></span>|<span data-ttu-id="b8af8-130">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-130">String</span></span>|<span data-ttu-id="b8af8-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="b8af8-131">Name of the entity.</span></span> <span data-ttu-id="b8af8-132">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b8af8-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b8af8-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b8af8-133">lastModifiedDateTime</span></span>|<span data-ttu-id="b8af8-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8af8-134">DateTimeOffset</span></span>|<span data-ttu-id="b8af8-135">オブジェクトが最後に変更された DateTime。</span><span class="sxs-lookup"><span data-stu-id="b8af8-135">Gets or sets a DateTime value specifying when the node object was last modified.</span></span> <span data-ttu-id="b8af8-136">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b8af8-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b8af8-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b8af8-137">createdDateTime</span></span>|<span data-ttu-id="b8af8-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8af8-138">DateTimeOffset</span></span>|<span data-ttu-id="b8af8-139">オブジェクトが作成された DateTime。</span><span class="sxs-lookup"><span data-stu-id="b8af8-139">DateTime the object was created.</span></span> <span data-ttu-id="b8af8-140">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b8af8-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b8af8-141">description</span><span class="sxs-lookup"><span data-stu-id="b8af8-141">description</span></span>|<span data-ttu-id="b8af8-142">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-142">String</span></span>|<span data-ttu-id="b8af8-143">デバイス構成について管理者が提供した説明。</span><span class="sxs-lookup"><span data-stu-id="b8af8-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="b8af8-144">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b8af8-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b8af8-145">displayName</span><span class="sxs-lookup"><span data-stu-id="b8af8-145">displayName</span></span>|<span data-ttu-id="b8af8-146">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-146">String</span></span>|<span data-ttu-id="b8af8-147">デバイス構成について管理者が指定した名前。</span><span class="sxs-lookup"><span data-stu-id="b8af8-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="b8af8-148">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b8af8-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b8af8-149">version</span><span class="sxs-lookup"><span data-stu-id="b8af8-149">version</span></span>|<span data-ttu-id="b8af8-150">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-150">Int32</span></span>|<span data-ttu-id="b8af8-151">デバイス構成のバージョン。</span><span class="sxs-lookup"><span data-stu-id="b8af8-151">Version of the device configuration.</span></span> <span data-ttu-id="b8af8-152">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="b8af8-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="b8af8-153">enterpriseCloudPrintDiscoveryEndPoint</span><span class="sxs-lookup"><span data-stu-id="b8af8-153">enterpriseCloudPrintDiscoveryEndPoint</span></span>|<span data-ttu-id="b8af8-154">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-154">String</span></span>|<span data-ttu-id="b8af8-155">クラウド プリンターを検出するエンドポイント。</span><span class="sxs-lookup"><span data-stu-id="b8af8-155">Endpoint for discovering cloud printers.</span></span>|
|<span data-ttu-id="b8af8-156">enterpriseCloudPrintOAuthAuthority</span><span class="sxs-lookup"><span data-stu-id="b8af8-156">enterpriseCloudPrintOAuthAuthority</span></span>|<span data-ttu-id="b8af8-157">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-157">String</span></span>|<span data-ttu-id="b8af8-158">OAuth トークンを取得するための認証エンドポイント。</span><span class="sxs-lookup"><span data-stu-id="b8af8-158">Authentication endpoint for acquiring OAuth tokens.</span></span>|
|<span data-ttu-id="b8af8-159">enterpriseCloudPrintOAuthClientIdentifier</span><span class="sxs-lookup"><span data-stu-id="b8af8-159">enterpriseCloudPrintOAuthClientIdentifier</span></span>|<span data-ttu-id="b8af8-160">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-160">String</span></span>|<span data-ttu-id="b8af8-161">OAuth 認証機関から OAuth トークンを取得することを承認されているクライアント アプリケーションの GUID。</span><span class="sxs-lookup"><span data-stu-id="b8af8-161">GUID of a client application authorized to retrieve OAuth tokens from the OAuth Authority.</span></span>|
|<span data-ttu-id="b8af8-162">enterpriseCloudPrintResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="b8af8-162">enterpriseCloudPrintResourceIdentifier</span></span>|<span data-ttu-id="b8af8-163">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-163">String</span></span>|<span data-ttu-id="b8af8-164">Azure Portal で構成されている印刷サービスの OAuth リソース URI。</span><span class="sxs-lookup"><span data-stu-id="b8af8-164">OAuth resource URI for print service as configured in the Azure portal.</span></span>|
|<span data-ttu-id="b8af8-165">enterpriseCloudPrintDiscoveryMaxLimit</span><span class="sxs-lookup"><span data-stu-id="b8af8-165">enterpriseCloudPrintDiscoveryMaxLimit</span></span>|<span data-ttu-id="b8af8-166">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-166">Int32</span></span>|<span data-ttu-id="b8af8-167">検出エンドポイントからクエリを実行する必要があるプリンターの最大数。</span><span class="sxs-lookup"><span data-stu-id="b8af8-167">Maximum number of printers that should be queried from a discovery endpoint.</span></span> <span data-ttu-id="b8af8-168">これはモバイルのみでの設定です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-168">This is a mobile only setting.</span></span> <span data-ttu-id="b8af8-169">有効な値は 1 から 65535 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-169">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="b8af8-170">enterpriseCloudPrintMopriaDiscoveryResourceIdentifier</span><span class="sxs-lookup"><span data-stu-id="b8af8-170">enterpriseCloudPrintMopriaDiscoveryResourceIdentifier</span></span>|<span data-ttu-id="b8af8-171">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-171">String</span></span>|<span data-ttu-id="b8af8-172">Azure Portal で構成されているプリンター検出サービスの OAuth リソース URI。</span><span class="sxs-lookup"><span data-stu-id="b8af8-172">OAuth resource URI for printer discovery service as configured in Azure portal.</span></span>|
|<span data-ttu-id="b8af8-173">searchBlockDiacritics</span><span class="sxs-lookup"><span data-stu-id="b8af8-173">searchBlockDiacritics</span></span>|<span data-ttu-id="b8af8-174">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-174">Boolean</span></span>|<span data-ttu-id="b8af8-175">検索で分音記号を使用できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-175">Specifies if search can use diacritics.</span></span>|
|<span data-ttu-id="b8af8-176">searchDisableAutoLanguageDetection</span><span class="sxs-lookup"><span data-stu-id="b8af8-176">searchDisableAutoLanguageDetection</span></span>|<span data-ttu-id="b8af8-177">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-177">Boolean</span></span>|<span data-ttu-id="b8af8-178">コンテンツとプロパティのインデックスを作成するときに、自動言語検出を使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-178">Specifies whether to use automatic language detection when indexing content and properties.</span></span>|
|<span data-ttu-id="b8af8-179">searchDisableIndexingEncryptedItems</span><span class="sxs-lookup"><span data-stu-id="b8af8-179">searchDisableIndexingEncryptedItems</span></span>|<span data-ttu-id="b8af8-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-180">Boolean</span></span>|<span data-ttu-id="b8af8-181">Cortana またはエクスプローラーの検索結果に表示されないようにするため、WIP で保護されているアイテムのインデックス作成を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-181">Indicates whether or not to block indexing of WIP-protected items to prevent them from appearing in search results for Cortana or Explorer.</span></span>|
|<span data-ttu-id="b8af8-182">searchEnableRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="b8af8-182">searchEnableRemoteQueries</span></span>|<span data-ttu-id="b8af8-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-183">Boolean</span></span>|<span data-ttu-id="b8af8-184">このコンピューターのインデックスに対するリモート クエリをブロックするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-184">Indicates whether or not to block remote queries of this computer’s index.</span></span>|
|<span data-ttu-id="b8af8-185">searchDisableIndexerBackoff</span><span class="sxs-lookup"><span data-stu-id="b8af8-185">searchDisableIndexerBackoff</span></span>|<span data-ttu-id="b8af8-186">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-186">Boolean</span></span>|<span data-ttu-id="b8af8-187">インデクサー バックオフの検索機能を無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-187">Indicates whether or not to disable the search indexer backoff feature.</span></span>|
|<span data-ttu-id="b8af8-188">searchDisableIndexingRemovableDrive</span><span class="sxs-lookup"><span data-stu-id="b8af8-188">searchDisableIndexingRemovableDrive</span></span>|<span data-ttu-id="b8af8-189">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-189">Boolean</span></span>|<span data-ttu-id="b8af8-190">リムーバブル ドライブ上の場所をライブラリに追加してインデックスを作成することをユーザーに許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-190">Indicates whether or not to allow users to add locations on removable drives to libraries and to be indexed.</span></span>|
|<span data-ttu-id="b8af8-191">searchEnableAutomaticIndexSizeManangement</span><span class="sxs-lookup"><span data-stu-id="b8af8-191">searchEnableAutomaticIndexSizeManangement</span></span>|<span data-ttu-id="b8af8-192">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-192">Boolean</span></span>|<span data-ttu-id="b8af8-193">インデックスの場所と同じドライブ上のハード ドライブ領域の最小値を指定して、その最小値を下回ったらインデックス作成を停止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-193">Specifies minimum amount of hard drive space on the same drive as the index location before indexing stops.</span></span>|
|<span data-ttu-id="b8af8-194">diagnosticsDataSubmissionMode</span><span class="sxs-lookup"><span data-stu-id="b8af8-194">diagnosticsDataSubmissionMode</span></span>|<span data-ttu-id="b8af8-195">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-195">String</span></span>|<span data-ttu-id="b8af8-196">診断データと利用統計情報データ (Watson など) の送信をデバイスに許可する値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-196">Gets or sets a value allowing the device to send diagnostic and usage telemetry data, such as Watson.</span></span> <span data-ttu-id="b8af8-197">可能な値は、`userDefined`、`none`、`basic`、`enhanced`、`full` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-197">Possible values are: `userDefined`, `none`, `basic`, `enhanced`, `full`.</span></span>|
|<span data-ttu-id="b8af8-198">oneDriveDisableFileSync</span><span class="sxs-lookup"><span data-stu-id="b8af8-198">oneDriveDisableFileSync</span></span>|<span data-ttu-id="b8af8-199">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-199">Boolean</span></span>|<span data-ttu-id="b8af8-200">アプリや機能から OneDrive 上のファイルを操作することを IT 管理者が禁止できるかどうかを示す値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-200">Gets or sets a value allowing IT admins to prevent apps and features from working with files on OneDrive.</span></span>|
|<span data-ttu-id="b8af8-201">smartScreenEnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="b8af8-201">smartScreenEnableAppInstallControl</span></span>|<span data-ttu-id="b8af8-202">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-202">Boolean</span></span>|<span data-ttu-id="b8af8-203">ユーザーがストア以外の場所からアプリをインストールできるかどうかを IT 管理者が制御することを許可します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-203">Allows IT Admins to control whether users are allowed to install apps from places other than the Store.</span></span>|
|<span data-ttu-id="b8af8-204">personalizationDesktopImageUrl</span><span class="sxs-lookup"><span data-stu-id="b8af8-204">personalizationDesktopImageUrl</span></span>|<span data-ttu-id="b8af8-205">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-205">String</span></span>|<span data-ttu-id="b8af8-206">ダウンロードしてデスクトップ画像として使用する必要がある jpg、jpeg、png 画像の http または https URL、あるいはデスクトップ画像として使用する必要があるファイル システム上のローカル画像のファイル URL。</span><span class="sxs-lookup"><span data-stu-id="b8af8-206">A http or https Url to a jpg, jpeg or png image that needs to be downloaded and used as the Desktop Image or a file Url to a local image on the file system that needs to used as the Desktop Image.</span></span>|
|<span data-ttu-id="b8af8-207">personalizationLockScreenImageUrl</span><span class="sxs-lookup"><span data-stu-id="b8af8-207">personalizationLockScreenImageUrl</span></span>|<span data-ttu-id="b8af8-208">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-208">String</span></span>|<span data-ttu-id="b8af8-209">ダウンロードしてロック画面画像として使用する必要がある jpg、jpeg、png 画像の http または https URL、あるいはロック画面画像として使用する必要があるファイル システム上のローカル画像のファイル URL。</span><span class="sxs-lookup"><span data-stu-id="b8af8-209">A http or https Url to a jpg, jpeg or png image that neeeds to be downloaded and used as the Lock Screen Image or a file Url to a local image on the file system that needs to be used as the Lock Screen Image.</span></span>|
|<span data-ttu-id="b8af8-210">bluetoothAllowedServices</span><span class="sxs-lookup"><span data-stu-id="b8af8-210">bluetoothAllowedServices</span></span>|<span data-ttu-id="b8af8-211">String コレクション</span><span class="sxs-lookup"><span data-stu-id="b8af8-211">String collection</span></span>|<span data-ttu-id="b8af8-212">許可されている Bluetooth サービスおよびプロファイルの一覧を 16 進形式の文字列として指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-212">Specify a list of allowed Bluetooth services and profiles in hex formatted strings.</span></span>|
|<span data-ttu-id="b8af8-213">bluetoothBlockAdvertising</span><span class="sxs-lookup"><span data-stu-id="b8af8-213">bluetoothBlockAdvertising</span></span>|<span data-ttu-id="b8af8-214">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-214">Boolean</span></span>|<span data-ttu-id="b8af8-215">ユーザーが Bluetooth 広告を使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-215">Whether or not to Block the user from using bluetooth advertising.</span></span>|
|<span data-ttu-id="b8af8-216">bluetoothBlockDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="b8af8-216">bluetoothBlockDiscoverableMode</span></span>|<span data-ttu-id="b8af8-217">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-217">Boolean</span></span>|<span data-ttu-id="b8af8-218">ユーザーが Bluetooth の発見可能モードを使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-218">Whether or not to Block the user from using bluetooth discoverable mode.</span></span>|
|<span data-ttu-id="b8af8-219">bluetoothBlockPrePairing</span><span class="sxs-lookup"><span data-stu-id="b8af8-219">bluetoothBlockPrePairing</span></span>|<span data-ttu-id="b8af8-220">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-220">Boolean</span></span>|<span data-ttu-id="b8af8-221">バンドルされた特定のいくつかの Bluetooth 周辺機器を自動的にホスト デバイスとペアにすることを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-221">Whether or not to block specific bundled Bluetooth peripherals to automatically pair with the host device.</span></span>|
|<span data-ttu-id="b8af8-222">edgeBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="b8af8-222">edgeBlockAutofill</span></span>|<span data-ttu-id="b8af8-223">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-223">Boolean</span></span>|<span data-ttu-id="b8af8-224">自動入力を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-224">Indicates whether or not to block auto fill.</span></span>|
|<span data-ttu-id="b8af8-225">edgeBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-225">edgeBlocked</span></span>|<span data-ttu-id="b8af8-226">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-226">Boolean</span></span>|<span data-ttu-id="b8af8-227">ユーザーが Edge ブラウザーを使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-227">Indicates whether or not to Block the user from using the Edge browser.</span></span>|
|<span data-ttu-id="b8af8-228">edgeCookiePolicy</span><span class="sxs-lookup"><span data-stu-id="b8af8-228">edgeCookiePolicy</span></span>|<span data-ttu-id="b8af8-229">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-229">String</span></span>|<span data-ttu-id="b8af8-230">Edge ブラウザーでどの Cookie を禁止するかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-230">Indicates which cookies to block in the Edge browser.</span></span> <span data-ttu-id="b8af8-231">可能な値は、`userDefined`、`allow`、`blockThirdParty`、`blockAll` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-231">Possible values are: `userDefined`, `allow`, `blockThirdParty`, `blockAll`.</span></span>|
|<span data-ttu-id="b8af8-232">edgeBlockDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="b8af8-232">edgeBlockDeveloperTools</span></span>|<span data-ttu-id="b8af8-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-233">Boolean</span></span>|<span data-ttu-id="b8af8-234">Edge ブラウザー内の開発者ツールを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-234">Indicates whether or not to block developer tools in the Edge browser.</span></span>|
|<span data-ttu-id="b8af8-235">edgeBlockSendingDoNotTrackHeader</span><span class="sxs-lookup"><span data-stu-id="b8af8-235">edgeBlockSendingDoNotTrackHeader</span></span>|<span data-ttu-id="b8af8-236">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-236">Boolean</span></span>|<span data-ttu-id="b8af8-237">ユーザーがトラッキング拒否ヘッダーを送信することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-237">Indicates whether or not to Block the user from sending the do not track header.</span></span>|
|<span data-ttu-id="b8af8-238">edgeBlockExtensions</span><span class="sxs-lookup"><span data-stu-id="b8af8-238">edgeBlockExtensions</span></span>|<span data-ttu-id="b8af8-239">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-239">Boolean</span></span>|<span data-ttu-id="b8af8-240">Edge ブラウザーの拡張機能を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-240">Indicates whether or not to block extensions in the Edge browser.</span></span>|
|<span data-ttu-id="b8af8-241">edgeBlockInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="b8af8-241">edgeBlockInPrivateBrowsing</span></span>|<span data-ttu-id="b8af8-242">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-242">Boolean</span></span>|<span data-ttu-id="b8af8-243">Edge ブラウザーで会社のネットワークの InPrivate ブラウズを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-243">Indicates whether or not to block InPrivate browsing on corporate networks, in the Edge browser.</span></span>|
|<span data-ttu-id="b8af8-244">edgeBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="b8af8-244">edgeBlockJavaScript</span></span>|<span data-ttu-id="b8af8-245">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-245">Boolean</span></span>|<span data-ttu-id="b8af8-246">ユーザーが JavaScript を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-246">Indicates whether or not to Block the user from using JavaScript.</span></span>|
|<span data-ttu-id="b8af8-247">edgeBlockPasswordManager</span><span class="sxs-lookup"><span data-stu-id="b8af8-247">edgeBlockPasswordManager</span></span>|<span data-ttu-id="b8af8-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-248">Boolean</span></span>|<span data-ttu-id="b8af8-249">パスワード マネージャーを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-249">Indicates whether or not to Block password manager.</span></span>|
|<span data-ttu-id="b8af8-250">edgeBlockAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="b8af8-250">edgeBlockAddressBarDropdown</span></span>|<span data-ttu-id="b8af8-251">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-251">Boolean</span></span>|<span data-ttu-id="b8af8-252">Microsoft Edge のアドレス バー ドロップダウン機能を禁止します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-252">Block the address bar dropdown functionality in Microsoft Edge.</span></span> <span data-ttu-id="b8af8-253">Microsoft Edge から Microsoft サービスへのネットワーク接続を最小限に抑えるには、この設定を無効にします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-253">Disable this settings to minimize network connections from Microsoft Edge to Microsoft services.</span></span>|
|<span data-ttu-id="b8af8-254">edgeBlockCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="b8af8-254">edgeBlockCompatibilityList</span></span>|<span data-ttu-id="b8af8-255">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-255">Boolean</span></span>|<span data-ttu-id="b8af8-256">Microsoft Edge での Microsoft 互換性リストを禁止します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-256">Block Microsoft compatibility list in Microsoft Edge.</span></span> <span data-ttu-id="b8af8-257">Microsoft ではこのリストを利用して、既知の互換性の問題があるサイトを Edge で正しく表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-257">This list from Microsoft helps Edge properly display sites with known compatibility issues.</span></span>|
|<span data-ttu-id="b8af8-258">edgeClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="b8af8-258">edgeClearBrowsingDataOnExit</span></span>|<span data-ttu-id="b8af8-259">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-259">Boolean</span></span>|<span data-ttu-id="b8af8-260">Microsoft Edge の終了時にブラウズ データを消去します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-260">Clear browsing data on exiting Microsoft Edge.</span></span>|
|<span data-ttu-id="b8af8-261">edgeAllowStartPagesModification</span><span class="sxs-lookup"><span data-stu-id="b8af8-261">edgeAllowStartPagesModification</span></span>|<span data-ttu-id="b8af8-262">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-262">Boolean</span></span>|<span data-ttu-id="b8af8-263">Edge のスタート ページをユーザーが変更することを許可します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-263">Allow users to change Start pages on Edge.</span></span> <span data-ttu-id="b8af8-264">ユーザーが Edge を開いたときに既定で表示されるスタート ページを指定するには、EdgeHomepageUrls を使用します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-264">Use the EdgeHomepageUrls to specify the Start pages that the user would see by default when they open Edge.</span></span>|
|<span data-ttu-id="b8af8-265">edgeDisableFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-265">edgeDisableFirstRunPage</span></span>|<span data-ttu-id="b8af8-266">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-266">Boolean</span></span>|<span data-ttu-id="b8af8-267">Microsoft Edge の初回使用時に表示される Microsoft の Web ページを禁止します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-267">Block the Microsoft web page that opens on the first use of Microsoft Edge.</span></span> <span data-ttu-id="b8af8-268">このポリシーでは、ゼロ エミッション構成に登録している企業などが、このページの表示を禁止できます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-268">This policy allows enterprises, like those enrolled in zero emissions configurations, to block this page.</span></span>|
|<span data-ttu-id="b8af8-269">edgeBlockLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="b8af8-269">edgeBlockLiveTileDataCollection</span></span>|<span data-ttu-id="b8af8-270">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-270">Boolean</span></span>|<span data-ttu-id="b8af8-271">ユーザーが Microsoft Edge からスタートにサイトをピン留めしたときに、ライブ タイルを作成するために Microsoft が情報を収集することを禁止します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-271">Block the collection of information by Microsoft for live tile creation when users pin a site to Start from Microsoft Edge.</span></span>|
|<span data-ttu-id="b8af8-272">edgeSyncFavoritesWithInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="b8af8-272">edgeSyncFavoritesWithInternetExplorer</span></span>|<span data-ttu-id="b8af8-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-273">Boolean</span></span>|<span data-ttu-id="b8af8-274">Internet Explorer と Microsoft Edge の間でお気に入りの同期を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-274">Enable favorites sync between Internet Explorer and Microsoft Edge.</span></span> <span data-ttu-id="b8af8-275">お気に入りの追加、削除、変更、順序変更が、ブラウザー間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-275">Additions, deletions, modifications and order changes to favorites are shared between browsers.</span></span>|
|<span data-ttu-id="b8af8-276">cellularBlockDataWhenRoaming</span><span class="sxs-lookup"><span data-stu-id="b8af8-276">cellularBlockDataWhenRoaming</span></span>|<span data-ttu-id="b8af8-277">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-277">Boolean</span></span>|<span data-ttu-id="b8af8-278">ローミング中に携帯電話上でユーザーがデータを使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-278">Whether or not to Block the user from using data over cellular while roaming.</span></span>|
|<span data-ttu-id="b8af8-279">cellularBlockVpn</span><span class="sxs-lookup"><span data-stu-id="b8af8-279">cellularBlockVpn</span></span>|<span data-ttu-id="b8af8-280">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-280">Boolean</span></span>|<span data-ttu-id="b8af8-281">携帯電話上でユーザーが VPN を使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-281">Whether or not to Block the user from using VPN over cellular.</span></span>|
|<span data-ttu-id="b8af8-282">cellularBlockVpnWhenRoaming</span><span class="sxs-lookup"><span data-stu-id="b8af8-282">cellularBlockVpnWhenRoaming</span></span>|<span data-ttu-id="b8af8-283">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-283">Boolean</span></span>|<span data-ttu-id="b8af8-284">ローミング時に携帯電話上でユーザーが VPN を使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-284">Whether or not to Block the user from using VPN when roaming over cellular.</span></span>|
|<span data-ttu-id="b8af8-285">defenderBlockEndUserAccess</span><span class="sxs-lookup"><span data-stu-id="b8af8-285">defenderBlockEndUserAccess</span></span>|<span data-ttu-id="b8af8-286">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-286">Boolean</span></span>|<span data-ttu-id="b8af8-287">エンド ユーザーが Defender にアクセスすることを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-287">Whether or not to block end user access to Defender.</span></span>|
|<span data-ttu-id="b8af8-288">defenderDaysBeforeDeletingQuarantinedMalware</span><span class="sxs-lookup"><span data-stu-id="b8af8-288">defenderDaysBeforeDeletingQuarantinedMalware</span></span>|<span data-ttu-id="b8af8-289">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-289">Int32</span></span>|<span data-ttu-id="b8af8-290">検疫済みのマルウェアを削除するまでの日数。</span><span class="sxs-lookup"><span data-stu-id="b8af8-290">Number of days before deleting quarantined malware.</span></span> <span data-ttu-id="b8af8-291">有効な値は 0 から 90 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-291">Valid values 0 to 90</span></span>|
|<span data-ttu-id="b8af8-292">defenderDetectedMalwareActions</span><span class="sxs-lookup"><span data-stu-id="b8af8-292">defenderDetectedMalwareActions</span></span>|[<span data-ttu-id="b8af8-293">defenderDetectedMalwareActions</span><span class="sxs-lookup"><span data-stu-id="b8af8-293">defenderDetectedMalwareActions</span></span>](../resources/intune_deviceconfig_defenderdetectedmalwareactions.md)|<span data-ttu-id="b8af8-294">検出されたマルウェアに対する Defender のアクションを脅威レベルごとに取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-294">Gets or sets Defender’s actions to take on detected Malware per threat level.</span></span>|
|<span data-ttu-id="b8af8-295">defenderSystemScanSchedule</span><span class="sxs-lookup"><span data-stu-id="b8af8-295">defenderSystemScanSchedule</span></span>|<span data-ttu-id="b8af8-296">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-296">String</span></span>|<span data-ttu-id="b8af8-297">Defender がシステムをスキャンする曜日。</span><span class="sxs-lookup"><span data-stu-id="b8af8-297">Defender day of the week for the system scan.</span></span> <span data-ttu-id="b8af8-298">可能な値は、`userDefined`、`everyday`、`sunday`、`monday`、`tuesday`、`wednesday`、`thursday`、`friday`、`saturday` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-298">Possible values are: `userDefined`, `everyday`, `sunday`, `monday`, `tuesday`, `wednesday`, `thursday`.</span></span>|
|<span data-ttu-id="b8af8-299">defenderFilesAndFoldersToExclude</span><span class="sxs-lookup"><span data-stu-id="b8af8-299">defenderFilesAndFoldersToExclude</span></span>|<span data-ttu-id="b8af8-300">String コレクション</span><span class="sxs-lookup"><span data-stu-id="b8af8-300">String collection</span></span>|<span data-ttu-id="b8af8-301">スキャンとリアルタイム保護から除外するファイルとフォルダー。</span><span class="sxs-lookup"><span data-stu-id="b8af8-301">Files and folder to exclude from scans and real time protection.</span></span>|
|<span data-ttu-id="b8af8-302">defenderFileExtensionsToExclude</span><span class="sxs-lookup"><span data-stu-id="b8af8-302">defenderFileExtensionsToExclude</span></span>|<span data-ttu-id="b8af8-303">String コレクション</span><span class="sxs-lookup"><span data-stu-id="b8af8-303">String collection</span></span>|<span data-ttu-id="b8af8-304">スキャンとリアルタイム保護から除外するファイル拡張子。</span><span class="sxs-lookup"><span data-stu-id="b8af8-304">File extensions to exclude from scans and real time protection.</span></span>|
|<span data-ttu-id="b8af8-305">defenderScanMaxCpu</span><span class="sxs-lookup"><span data-stu-id="b8af8-305">defenderScanMaxCpu</span></span>|<span data-ttu-id="b8af8-306">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-306">Int32</span></span>|<span data-ttu-id="b8af8-307">スキャン中の最大 CPU 使用率。</span><span class="sxs-lookup"><span data-stu-id="b8af8-307">Max CPU usage percentage during scan.</span></span> <span data-ttu-id="b8af8-308">有効な値は 0 から 100 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-308">Valid values 0 to 100</span></span>|
|<span data-ttu-id="b8af8-309">defenderMonitorFileActivity</span><span class="sxs-lookup"><span data-stu-id="b8af8-309">defenderMonitorFileActivity</span></span>|<span data-ttu-id="b8af8-310">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-310">String</span></span>|<span data-ttu-id="b8af8-311">ファイル アクティビティを監視する値。</span><span class="sxs-lookup"><span data-stu-id="b8af8-311">Value for monitoring file activity.</span></span> <span data-ttu-id="b8af8-312">可能な値は、`userDefined`、`disable`、`monitorAllFiles`、`monitorIncomingFilesOnly`、`monitorOutgoingFilesOnly` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-312">Possible values are: `userDefined`, `disable`, `monitorAllFiles`, `monitorIncomingFilesOnly`, `monitorOutgoingFilesOnly`.</span></span>|
|<span data-ttu-id="b8af8-313">defenderProcessesToExclude</span><span class="sxs-lookup"><span data-stu-id="b8af8-313">defenderProcessesToExclude</span></span>|<span data-ttu-id="b8af8-314">String コレクション</span><span class="sxs-lookup"><span data-stu-id="b8af8-314">String collection</span></span>|<span data-ttu-id="b8af8-315">スキャンとリアルタイム保護から除外するプロセス。</span><span class="sxs-lookup"><span data-stu-id="b8af8-315">Processes to exclude from scans and real time protection.</span></span>|
|<span data-ttu-id="b8af8-316">defenderPromptForSampleSubmission</span><span class="sxs-lookup"><span data-stu-id="b8af8-316">defenderPromptForSampleSubmission</span></span>|<span data-ttu-id="b8af8-317">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-317">String</span></span>|<span data-ttu-id="b8af8-318">ユーザーにサンプルの送信を要求する方法の構成。</span><span class="sxs-lookup"><span data-stu-id="b8af8-318">The configuration for how to prompt user for sample submission.</span></span> <span data-ttu-id="b8af8-319">可能な値は、`userDefined`、`alwaysPrompt`、`promptBeforeSendingPersonalData`、`neverSendData`、`sendAllDataWithoutPrompting` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-319">Possible values are: `userDefined`, `alwaysPrompt`, `promptBeforeSendingPersonalData`, `neverSendData`, `sendAllDataWithoutPrompting`.</span></span>|
|<span data-ttu-id="b8af8-320">defenderRequireBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="b8af8-320">defenderRequireBehaviorMonitoring</span></span>|<span data-ttu-id="b8af8-321">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-321">Boolean</span></span>|<span data-ttu-id="b8af8-322">動作の監視が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-322">Indicates whether or not to require behavior monitoring.</span></span>|
|<span data-ttu-id="b8af8-323">defenderRequireCloudProtection</span><span class="sxs-lookup"><span data-stu-id="b8af8-323">defenderRequireCloudProtection</span></span>|<span data-ttu-id="b8af8-324">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-324">Boolean</span></span>|<span data-ttu-id="b8af8-325">クラウドの保護が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-325">Indicates whether or not to require cloud protection.</span></span>|
|<span data-ttu-id="b8af8-326">defenderRequireNetworkInspectionSystem</span><span class="sxs-lookup"><span data-stu-id="b8af8-326">defenderRequireNetworkInspectionSystem</span></span>|<span data-ttu-id="b8af8-327">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-327">Boolean</span></span>|<span data-ttu-id="b8af8-328">ネットワーク検査システムが必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-328">Indicates whether or not to require network inspection system.</span></span>|
|<span data-ttu-id="b8af8-329">defenderRequireRealTimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="b8af8-329">defenderRequireRealTimeMonitoring</span></span>|<span data-ttu-id="b8af8-330">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-330">Boolean</span></span>|<span data-ttu-id="b8af8-331">リアルタイムの監視が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-331">Indicates whether or not to require real time monitoring.</span></span>|
|<span data-ttu-id="b8af8-332">defenderScanArchiveFiles</span><span class="sxs-lookup"><span data-stu-id="b8af8-332">defenderScanArchiveFiles</span></span>|<span data-ttu-id="b8af8-333">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-333">Boolean</span></span>|<span data-ttu-id="b8af8-334">アーカイブ ファイルをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-334">Indicates whether or not to scan archive files.</span></span>|
|<span data-ttu-id="b8af8-335">defenderScanDownloads</span><span class="sxs-lookup"><span data-stu-id="b8af8-335">defenderScanDownloads</span></span>|<span data-ttu-id="b8af8-336">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-336">Boolean</span></span>|<span data-ttu-id="b8af8-337">ダウンロードをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-337">Indicates whether or not to scan downloads.</span></span>|
|<span data-ttu-id="b8af8-338">defenderScanNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="b8af8-338">defenderScanNetworkFiles</span></span>|<span data-ttu-id="b8af8-339">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-339">Boolean</span></span>|<span data-ttu-id="b8af8-340">ネットワーク フォルダーから開かれたファイルをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-340">Indicates whether or not to scan files opened from a network folder.</span></span>|
|<span data-ttu-id="b8af8-341">defenderScanIncomingMail</span><span class="sxs-lookup"><span data-stu-id="b8af8-341">defenderScanIncomingMail</span></span>|<span data-ttu-id="b8af8-342">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-342">Boolean</span></span>|<span data-ttu-id="b8af8-343">受信メール メッセージをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-343">Indicates whether or not to scan incoming mail messages.</span></span>|
|<span data-ttu-id="b8af8-344">defenderScanMappedNetworkDrivesDuringFullScan</span><span class="sxs-lookup"><span data-stu-id="b8af8-344">defenderScanMappedNetworkDrivesDuringFullScan</span></span>|<span data-ttu-id="b8af8-345">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-345">Boolean</span></span>|<span data-ttu-id="b8af8-346">フル スキャン時に、マップされたネットワーク ドライブをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-346">Indicates whether or not to scan mapped network drives during full scan.</span></span>|
|<span data-ttu-id="b8af8-347">defenderScanRemovableDrivesDuringFullScan</span><span class="sxs-lookup"><span data-stu-id="b8af8-347">defenderScanRemovableDrivesDuringFullScan</span></span>|<span data-ttu-id="b8af8-348">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-348">Boolean</span></span>|<span data-ttu-id="b8af8-349">フル スキャン時に、リムーバブル ドライブをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-349">Indicates whether or not to scan removable drives during full scan.</span></span>|
|<span data-ttu-id="b8af8-350">defenderScanScriptsLoadedInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="b8af8-350">defenderScanScriptsLoadedInInternetExplorer</span></span>|<span data-ttu-id="b8af8-351">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-351">Boolean</span></span>|<span data-ttu-id="b8af8-352">Internet Explorer ブラウザーに読み込まれるスクリプトをスキャンするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-352">Indicates whether or not to scan scripts loaded in Internet Explorer browser.</span></span>|
|<span data-ttu-id="b8af8-353">defenderSignatureUpdateIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="b8af8-353">defenderSignatureUpdateIntervalInHours</span></span>|<span data-ttu-id="b8af8-354">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-354">Int32</span></span>|<span data-ttu-id="b8af8-355">署名を更新する間隔 (時間)。</span><span class="sxs-lookup"><span data-stu-id="b8af8-355">The signature update interval in hours.</span></span> <span data-ttu-id="b8af8-356">確認しない場合は 0 を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-356">Specify 0 not to check.</span></span> <span data-ttu-id="b8af8-357">有効な値は 0 から 24 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-357">Valid values 0 to 24</span></span>|
|<span data-ttu-id="b8af8-358">defenderScanType</span><span class="sxs-lookup"><span data-stu-id="b8af8-358">defenderScanType</span></span>|<span data-ttu-id="b8af8-359">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-359">String</span></span>|<span data-ttu-id="b8af8-360">Defender システム スキャンの種類。</span><span class="sxs-lookup"><span data-stu-id="b8af8-360">The defender system scan type.</span></span> <span data-ttu-id="b8af8-361">可能な値は、`userDefined`、`disabled`、`quick`、`full` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-361">Possible values are: `userDefined`, `disabled`, `quick`, `full`.</span></span>|
|<span data-ttu-id="b8af8-362">defenderScheduledScanTime</span><span class="sxs-lookup"><span data-stu-id="b8af8-362">defenderScheduledScanTime</span></span>|<span data-ttu-id="b8af8-363">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="b8af8-363">TimeOfDay</span></span>|<span data-ttu-id="b8af8-364">システムのスキャンの Defender 時刻。</span><span class="sxs-lookup"><span data-stu-id="b8af8-364">The defender time for the system scan.</span></span>|
|<span data-ttu-id="b8af8-365">defenderScheduledQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="b8af8-365">defenderScheduledQuickScanTime</span></span>|<span data-ttu-id="b8af8-366">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="b8af8-366">TimeOfDay</span></span>|<span data-ttu-id="b8af8-367">毎日のクイック スキャンを実行する時刻。</span><span class="sxs-lookup"><span data-stu-id="b8af8-367">The time to perform a daily quick scan.</span></span>|
|<span data-ttu-id="b8af8-368">defenderCloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="b8af8-368">defenderCloudBlockLevel</span></span>|<span data-ttu-id="b8af8-369">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-369">String</span></span>|<span data-ttu-id="b8af8-370">クラウド配信の保護レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-370">Specifies the level of cloud-delivered protection.</span></span> <span data-ttu-id="b8af8-371">可能な値は、`notConfigured`、`high`、`highPlus`、`zeroTolerance` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-371">Possible values are: `notConfigured`, `high`, `highPlus`, `zeroTolerance`.</span></span>|
|<span data-ttu-id="b8af8-372">lockScreenAllowTimeoutConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8af8-372">lockScreenAllowTimeoutConfiguration</span></span>|<span data-ttu-id="b8af8-373">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-373">Boolean</span></span>|<span data-ttu-id="b8af8-374">Windows 10 Mobile デバイスのロック画面で、画面のタイムアウトを制御するユーザー構成可能な設定を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-374">Specify whether to show a user-configurable setting to control the screen timeout while on the lock screen of Windows 10 Mobile devices.</span></span> <span data-ttu-id="b8af8-375">このポリシーが [許可] に設定されている場合は、lockScreenTimeoutInSeconds によって設定された値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-375">If this policy is set to Allow, the value set by lockScreenTimeoutInSeconds is ignored.</span></span>|
|<span data-ttu-id="b8af8-376">lockScreenBlockActionCenterNotifications</span><span class="sxs-lookup"><span data-stu-id="b8af8-376">lockScreenBlockActionCenterNotifications</span></span>|<span data-ttu-id="b8af8-377">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-377">Boolean</span></span>|<span data-ttu-id="b8af8-378">ロック画面上のアクション センター通知を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-378">Indicates whether or not to block action center notifications over lock screen.</span></span>|
|<span data-ttu-id="b8af8-379">lockScreenBlockCortana</span><span class="sxs-lookup"><span data-stu-id="b8af8-379">lockScreenBlockCortana</span></span>|<span data-ttu-id="b8af8-380">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-380">Boolean</span></span>|<span data-ttu-id="b8af8-381">システムのロック中にユーザーが音声認識を使用して Cortana と対話できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-381">Indicates whether or not the user can interact with Cortana using speech while the system is locked.</span></span>|
|<span data-ttu-id="b8af8-382">lockScreenBlockToastNotifications</span><span class="sxs-lookup"><span data-stu-id="b8af8-382">lockScreenBlockToastNotifications</span></span>|<span data-ttu-id="b8af8-383">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-383">Boolean</span></span>|<span data-ttu-id="b8af8-384">デバイスのロック画面へのトースト通知を許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-384">Indicates whether to allow toast notifications above the device lock screen.</span></span>|
|<span data-ttu-id="b8af8-385">lockScreenTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="b8af8-385">lockScreenTimeoutInSeconds</span></span>|<span data-ttu-id="b8af8-386">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-386">Int32</span></span>|<span data-ttu-id="b8af8-387">Windows 10 Mobile デバイスで画面をロックしてから画面をオフにするまでの時間 (秒) を設定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-387">Set the duration (in seconds) from the screen locking to the screen turning off for Windows 10 Mobile devices.</span></span> <span data-ttu-id="b8af8-388">サポートされている値は 11 から 1800 までです。</span><span class="sxs-lookup"><span data-stu-id="b8af8-388">Supported values are 11-1800.</span></span> <span data-ttu-id="b8af8-389">有効な値は 11 から 1800 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-389">Valid values 11 to 1800</span></span>|
|<span data-ttu-id="b8af8-390">passwordBlockSimple</span><span class="sxs-lookup"><span data-stu-id="b8af8-390">passwordBlockSimple</span></span>|<span data-ttu-id="b8af8-391">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-391">Boolean</span></span>|<span data-ttu-id="b8af8-392">"1111" や "1234" などの PIN またはパスワードを許可するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-392">Specify whether PINs or passwords such as "1111" or "1234" are allowed.</span></span> <span data-ttu-id="b8af8-393">Windows 10 デスクトップでは、ピクチャ パスワードの使用も制御します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-393">For Windows 10 desktops, it also controls the use of picture passwords.</span></span>|
|<span data-ttu-id="b8af8-394">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="b8af8-394">passwordExpirationDays</span></span>|<span data-ttu-id="b8af8-395">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-395">Int32</span></span>|<span data-ttu-id="b8af8-396">パスワードの有効期限 (日数)。</span><span class="sxs-lookup"><span data-stu-id="b8af8-396">The password expiration in days.</span></span> <span data-ttu-id="b8af8-397">有効な値は 0 から 730 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-397">Valid values 0 to 730</span></span>|
|<span data-ttu-id="b8af8-398">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="b8af8-398">passwordMinimumLength</span></span>|<span data-ttu-id="b8af8-399">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-399">Int32</span></span>|<span data-ttu-id="b8af8-400">パスワードの最小文字数。</span><span class="sxs-lookup"><span data-stu-id="b8af8-400">The minimum password length.</span></span> <span data-ttu-id="b8af8-401">有効な値は 4 から 16 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-401">Valid values 4 to 16</span></span>|
|<span data-ttu-id="b8af8-402">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="b8af8-402">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="b8af8-403">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-403">Int32</span></span>|<span data-ttu-id="b8af8-404">画面がタイムアウトになるまでの非アクティブ時間 (分)。</span><span class="sxs-lookup"><span data-stu-id="b8af8-404">The minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="b8af8-405">passwordMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="b8af8-405">passwordMinimumCharacterSetCount</span></span>|<span data-ttu-id="b8af8-406">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-406">Int32</span></span>|<span data-ttu-id="b8af8-407">パスワードに必要な文字セットの数。</span><span class="sxs-lookup"><span data-stu-id="b8af8-407">The number of character sets required in the password.</span></span>|
|<span data-ttu-id="b8af8-408">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="b8af8-408">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="b8af8-409">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-409">Int32</span></span>|<span data-ttu-id="b8af8-410">再使用を禁止する、以前のパスワードの数。</span><span class="sxs-lookup"><span data-stu-id="b8af8-410">The number of previous passwords to prevent reuse of.</span></span> <span data-ttu-id="b8af8-411">有効な値は 0 から 50 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-411">Valid values 0 to 50</span></span>|
|<span data-ttu-id="b8af8-412">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="b8af8-412">passwordRequired</span></span>|<span data-ttu-id="b8af8-413">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-413">Boolean</span></span>|<span data-ttu-id="b8af8-414">ユーザーにパスワードを要求するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-414">Indicates whether or not to require the user to have a password.</span></span>|
|<span data-ttu-id="b8af8-415">passwordRequireWhenResumeFromIdleState</span><span class="sxs-lookup"><span data-stu-id="b8af8-415">passwordRequireWhenResumeFromIdleState</span></span>|<span data-ttu-id="b8af8-416">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-416">Boolean</span></span>|<span data-ttu-id="b8af8-417">アイドル状態からの再開時にパスワードを要求するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-417">Indicates whether or not to require a password upon resuming from an idle state.</span></span>|
|<span data-ttu-id="b8af8-418">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="b8af8-418">passwordRequiredType</span></span>|<span data-ttu-id="b8af8-419">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-419">String</span></span>|<span data-ttu-id="b8af8-420">必要なパスワードの種類。</span><span class="sxs-lookup"><span data-stu-id="b8af8-420">The required password type.</span></span> <span data-ttu-id="b8af8-421">可能な値は、`deviceDefault`、`alphanumeric`、`numeric` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-421">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="b8af8-422">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="b8af8-422">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="b8af8-423">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-423">Int32</span></span>|<span data-ttu-id="b8af8-424">出荷時の設定にリセットされるサインインの失敗回数。</span><span class="sxs-lookup"><span data-stu-id="b8af8-424">The number of sign in failures before factory reset.</span></span> <span data-ttu-id="b8af8-425">有効な値は 0 から 999 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-425">Valid values 0 to 999</span></span>|
|<span data-ttu-id="b8af8-426">privacyAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="b8af8-426">privacyAdvertisingId</span></span>|<span data-ttu-id="b8af8-427">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-427">String</span></span>|<span data-ttu-id="b8af8-428">広告識別子の使用を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-428">Enables or disables the use of advertising ID.</span></span> <span data-ttu-id="b8af8-429">Windows 10 バージョン 1607 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="b8af8-429">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="b8af8-430">可能な値は、`notConfigured`、`blocked`、`allowed` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-430">Possible values are: `notConfigured`, `blocked`, `allowed`.</span></span>|
|<span data-ttu-id="b8af8-431">privacyAutoAcceptPairingAndConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="b8af8-431">privacyAutoAcceptPairingAndConsentPrompts</span></span>|<span data-ttu-id="b8af8-432">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-432">Boolean</span></span>|<span data-ttu-id="b8af8-433">アプリの起動時に、ペアリングとプライバシーに関するユーザーの同意ダイアログの自動受け入れを許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-433">Indicates whether or not to allow the automatic acceptance of the pairing and privacy user consent dialog when launching apps.</span></span>|
|<span data-ttu-id="b8af8-434">privacyBlockInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="b8af8-434">privacyBlockInputPersonalization</span></span>|<span data-ttu-id="b8af8-435">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-435">Boolean</span></span>|<span data-ttu-id="b8af8-436">Cortana、音声入力、ストア アプリケーションに対するクラウド ベースの音声サービスの使用を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-436">Indicates whether or not to block the usage of cloud based speech services for Cortana, Dictation, or Store applications.</span></span>|
|<span data-ttu-id="b8af8-437">startBlockUnpinningAppsFromTaskbar</span><span class="sxs-lookup"><span data-stu-id="b8af8-437">startBlockUnpinningAppsFromTaskbar</span></span>|<span data-ttu-id="b8af8-438">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-438">Boolean</span></span>|<span data-ttu-id="b8af8-439">ユーザーがタスク バーからアプリのピン留めを外すことを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-439">Indicates whether or not to block the user from unpinning apps from taskbar.</span></span>|
|<span data-ttu-id="b8af8-440">startMenuAppListVisibility</span><span class="sxs-lookup"><span data-stu-id="b8af8-440">startMenuAppListVisibility</span></span>|<span data-ttu-id="b8af8-441">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-441">String</span></span>|<span data-ttu-id="b8af8-442">この値を設定すると、アプリ リストを折りたたんだり、アプリ リスト全体を削除したり、設定アプリで対応する切り替えを無効にしたりできます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-442">Setting the value of this collapses the app list, removes the app list entirely, or disables the corresponding toggle in the Settings app.</span></span> <span data-ttu-id="b8af8-443">可能な値は、`userDefined`、`collapse`、`remove`、`disableSettingsApp` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-443">Possible values are: `userDefined`, `collapse`, `remove`, `disableSettingsApp`.</span></span>|
|<span data-ttu-id="b8af8-444">startMenuHideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="b8af8-444">startMenuHideChangeAccountSettings</span></span>|<span data-ttu-id="b8af8-445">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-445">Boolean</span></span>|<span data-ttu-id="b8af8-446">このポリシーを有効にすると、スタート メニューのユーザー タイルに [アカウント設定の変更] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-446">Enabling this policy hides the change account setting from appearing in the user tile in the start menu.</span></span>|
|<span data-ttu-id="b8af8-447">startMenuHideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="b8af8-447">startMenuHideFrequentlyUsedApps</span></span>|<span data-ttu-id="b8af8-448">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-448">Boolean</span></span>|<span data-ttu-id="b8af8-449">このポリシーを有効にすると、よく使われるアプリがスタート メニューに表示されなくなり、設定アプリで対応する切り替えが無効になります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-449">Enabling this policy hides the most used apps from appearing on the start menu and disables the corresponding toggle in the Settings app.</span></span>|
|<span data-ttu-id="b8af8-450">startMenuHideHibernate</span><span class="sxs-lookup"><span data-stu-id="b8af8-450">startMenuHideHibernate</span></span>|<span data-ttu-id="b8af8-451">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-451">Boolean</span></span>|<span data-ttu-id="b8af8-452">このポリシーを有効にすると、スタート メニューの電源ボタンに [休止状態] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-452">Enabling this policy hides hibernate from appearing in the power button in the start menu.</span></span>|
|<span data-ttu-id="b8af8-453">startMenuHideLock</span><span class="sxs-lookup"><span data-stu-id="b8af8-453">startMenuHideLock</span></span>|<span data-ttu-id="b8af8-454">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-454">Boolean</span></span>|<span data-ttu-id="b8af8-455">このポリシーを有効にすると、スタート メニューのユーザー タイルに [ロック] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-455">Enabling this policy hides lock from appearing in the user tile in the start menu.</span></span>|
|<span data-ttu-id="b8af8-456">startMenuHidePowerButton</span><span class="sxs-lookup"><span data-stu-id="b8af8-456">startMenuHidePowerButton</span></span>|<span data-ttu-id="b8af8-457">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-457">Boolean</span></span>|<span data-ttu-id="b8af8-458">このポリシーを有効にすると、スタート メニューに電源ボタンが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-458">Enabling this policy hides the power button from appearing in the start menu.</span></span>|
|<span data-ttu-id="b8af8-459">startMenuHideRecentJumpLists</span><span class="sxs-lookup"><span data-stu-id="b8af8-459">startMenuHideRecentJumpLists</span></span>|<span data-ttu-id="b8af8-460">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-460">Boolean</span></span>|<span data-ttu-id="b8af8-461">このポリシーを有効にすると、最近開いた項目のジャンプ リストがスタート メニュー/タスクバーに表示されなくなり、設定アプリで対応する切り替えが無効になります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-461">Enabling this policy hides recent jump lists from appearing on the start menu/taskbar and disables the corresponding toggle in the Settings app.</span></span>|
|<span data-ttu-id="b8af8-462">startMenuHideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="b8af8-462">startMenuHideRecentlyAddedApps</span></span>|<span data-ttu-id="b8af8-463">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-463">Boolean</span></span>|<span data-ttu-id="b8af8-464">このポリシーを有効にすると、最近追加したアプリがスタート メニューに表示されなくなり、設定アプリで対応する切り替えが無効になります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-464">Enabling this policy hides recently added apps from appearing on the start menu and disables the corresponding toggle in the Settings app.</span></span>|
|<span data-ttu-id="b8af8-465">startMenuHideRestartOptions</span><span class="sxs-lookup"><span data-stu-id="b8af8-465">startMenuHideRestartOptions</span></span>|<span data-ttu-id="b8af8-466">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-466">Boolean</span></span>|<span data-ttu-id="b8af8-467">このポリシーを有効にすると、スタート メニューの電源ボタンに [再起動]/[更新して再起動] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-467">Enabling this policy hides “Restart/Update and Restart” from appearing in the power button in the start menu.</span></span>|
|<span data-ttu-id="b8af8-468">startMenuHideShutDown</span><span class="sxs-lookup"><span data-stu-id="b8af8-468">startMenuHideShutDown</span></span>|<span data-ttu-id="b8af8-469">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-469">Boolean</span></span>|<span data-ttu-id="b8af8-470">このポリシーを有効にすると、スタート メニューの電源ボタンに [シャットダウン]/[更新してシャットダウン] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-470">Enabling this policy hides shut down/update and shut down from appearing in the power button in the start menu.</span></span>|
|<span data-ttu-id="b8af8-471">startMenuHideSignOut</span><span class="sxs-lookup"><span data-stu-id="b8af8-471">startMenuHideSignOut</span></span>|<span data-ttu-id="b8af8-472">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-472">Boolean</span></span>|<span data-ttu-id="b8af8-473">このポリシーを有効にすると、スタート メニューのユーザー タイルに [サインアウト] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-473">Enabling this policy hides sign out from appearing in the user tile in the start menu.</span></span>|
|<span data-ttu-id="b8af8-474">startMenuHideSleep</span><span class="sxs-lookup"><span data-stu-id="b8af8-474">startMenuHideSleep</span></span>|<span data-ttu-id="b8af8-475">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-475">Boolean</span></span>|<span data-ttu-id="b8af8-476">このポリシーを有効にすると、スタート メニューの電源ボタンに [スリープ] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-476">Enabling this policy hides sleep from appearing in the power button in the start menu.</span></span>|
|<span data-ttu-id="b8af8-477">startMenuHideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="b8af8-477">startMenuHideSwitchAccount</span></span>|<span data-ttu-id="b8af8-478">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-478">Boolean</span></span>|<span data-ttu-id="b8af8-479">このポリシーを有効にすると、スタート メニューのユーザー タイルに [アカウントの切り替え] が表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-479">Enabling this policy hides switch account from appearing in the user tile in the start menu.</span></span>|
|<span data-ttu-id="b8af8-480">startMenuHideUserTile</span><span class="sxs-lookup"><span data-stu-id="b8af8-480">startMenuHideUserTile</span></span>|<span data-ttu-id="b8af8-481">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-481">Boolean</span></span>|<span data-ttu-id="b8af8-482">このポリシーを有効にすると、スタート メニューにユーザー タイルが表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-482">Enabling this policy hides the user tile from appearing in the start menu.</span></span>|
|<span data-ttu-id="b8af8-483">startMenuLayoutEdgeAssetsXml</span><span class="sxs-lookup"><span data-stu-id="b8af8-483">startMenuLayoutEdgeAssetsXml</span></span>|<span data-ttu-id="b8af8-484">Binary</span><span class="sxs-lookup"><span data-stu-id="b8af8-484">Binary</span></span>|<span data-ttu-id="b8af8-485">このポリシー設定では、Edge アセットをインポートして startMenuLayoutXml ポリシーで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-485">This policy setting allows you to import Edge assets to be used with startMenuLayoutXml policy.</span></span> <span data-ttu-id="b8af8-486">スタートのレイアウトには、Edge アプリからのセカンダリ タイルを含めることができ、このタイルは Edge のローカル アセット ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-486">Start layout can contain secondary tile from Edge app which looks for Edge local asset file.</span></span> <span data-ttu-id="b8af8-487">Edge のローカル アセットは存在しないことがあり、その場合は Edge のセカンダリ タイルが空で表示されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-487">Edge local asset would not exist and cause Edge secondary tile to appear empty in this case.</span></span> <span data-ttu-id="b8af8-488">このポリシーは、startMenuLayoutXml ポリシーが変更された場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-488">This policy only gets applied when startMenuLayoutXml policy is modified.</span></span> <span data-ttu-id="b8af8-489">値は、UTF-8 の Base64 でエンコードされたバイト配列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-489">The value should be a UTF-8 Base64 encoded byte array.</span></span>|
|<span data-ttu-id="b8af8-490">startMenuLayoutXml</span><span class="sxs-lookup"><span data-stu-id="b8af8-490">startMenuLayoutXml</span></span>|<span data-ttu-id="b8af8-491">Binary</span><span class="sxs-lookup"><span data-stu-id="b8af8-491">Binary</span></span>|<span data-ttu-id="b8af8-492">管理者がスタート メニューの既定のレイアウトを上書きし、ユーザーがこれを変更できないようにすることを許可します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-492">Allows admins to override the default Start menu layout and prevents the user from changing it.</span></span> <span data-ttu-id="b8af8-493">レイアウトを変更するには、レイアウト変更スキーマに基づく XML ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-493">The layout is modified by specifying an XML file based on a layout modification schema.</span></span> <span data-ttu-id="b8af8-494">XML は、UTF8 エンコードのバイト配列形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b8af8-494">XML needs to be in a UTF8 encoded byte array format.</span></span>|
|<span data-ttu-id="b8af8-495">startMenuMode</span><span class="sxs-lookup"><span data-stu-id="b8af8-495">startMenuMode</span></span>|<span data-ttu-id="b8af8-496">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-496">String</span></span>|<span data-ttu-id="b8af8-497">管理者がスタート メニューの表示方法を決めることを許可します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-497">Allows admins to decide how the Start menu is displayed.</span></span> <span data-ttu-id="b8af8-498">可能な値は、`userDefined`、`fullScreen`、`nonFullScreen` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-498">Possible values are: `userDefined`, `fullScreen`, `nonFullScreen`.</span></span>|
|<span data-ttu-id="b8af8-499">startMenuPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="b8af8-499">startMenuPinnedFolderDocuments</span></span>|<span data-ttu-id="b8af8-500">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-500">String</span></span>|<span data-ttu-id="b8af8-501">スタート メニューへのドキュメント フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-501">Enforces the visibility (Show/Hide) of the Documents folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-502">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-502">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-503">startMenuPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="b8af8-503">startMenuPinnedFolderDownloads</span></span>|<span data-ttu-id="b8af8-504">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-504">String</span></span>|<span data-ttu-id="b8af8-505">スタート メニューへのダウンロード フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-505">Enforces the visibility (Show/Hide) of the Downloads folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-506">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-506">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-507">startMenuPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="b8af8-507">startMenuPinnedFolderFileExplorer</span></span>|<span data-ttu-id="b8af8-508">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-508">String</span></span>|<span data-ttu-id="b8af8-509">スタート メニューへのエクスプローラー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-509">Enforces the visibility (Show/Hide) of the FileExplorer shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-510">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-510">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-511">startMenuPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="b8af8-511">startMenuPinnedFolderHomeGroup</span></span>|<span data-ttu-id="b8af8-512">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-512">String</span></span>|<span data-ttu-id="b8af8-513">スタート メニューへのホームグループ フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-513">Enforces the visibility (Show/Hide) of the HomeGroup folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-514">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-514">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-515">startMenuPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="b8af8-515">startMenuPinnedFolderMusic</span></span>|<span data-ttu-id="b8af8-516">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-516">String</span></span>|<span data-ttu-id="b8af8-517">スタート メニューへのミュージック フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-517">Enforces the visibility (Show/Hide) of the Music folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-518">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-518">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-519">startMenuPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="b8af8-519">startMenuPinnedFolderNetwork</span></span>|<span data-ttu-id="b8af8-520">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-520">String</span></span>|<span data-ttu-id="b8af8-521">スタート メニューへのネットワーク フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-521">Enforces the visibility (Show/Hide) of the Network folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-522">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-522">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-523">startMenuPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="b8af8-523">startMenuPinnedFolderPersonalFolder</span></span>|<span data-ttu-id="b8af8-524">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-524">String</span></span>|<span data-ttu-id="b8af8-525">スタート メニューへの個人用フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-525">Enforces the visibility (Show/Hide) of the PersonalFolder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-526">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-526">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-527">startMenuPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="b8af8-527">startMenuPinnedFolderPictures</span></span>|<span data-ttu-id="b8af8-528">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-528">String</span></span>|<span data-ttu-id="b8af8-529">スタート メニューへのピクチャ フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-529">Enforces the visibility (Show/Hide) of the Pictures folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-530">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-530">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-531">startMenuPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="b8af8-531">startMenuPinnedFolderSettings</span></span>|<span data-ttu-id="b8af8-532">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-532">String</span></span>|<span data-ttu-id="b8af8-533">スタート メニューへの設定フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-533">Enforces the visibility (Show/Hide) of the Settings folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-534">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-534">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-535">startMenuPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="b8af8-535">startMenuPinnedFolderVideos</span></span>|<span data-ttu-id="b8af8-536">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-536">String</span></span>|<span data-ttu-id="b8af8-537">スタート メニューへのビデオ フォルダー ショートカットの表示/非表示を強制します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-537">Enforces the visibility (Show/Hide) of the Videos folder shortcut on the Start menu.</span></span> <span data-ttu-id="b8af8-538">可能な値は、`notConfigured`、`hide`、`show` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-538">Possible values are: `notConfigured`, `hide`, `show`.</span></span>|
|<span data-ttu-id="b8af8-539">settingsBlockSettingsApp</span><span class="sxs-lookup"><span data-stu-id="b8af8-539">settingsBlockSettingsApp</span></span>|<span data-ttu-id="b8af8-540">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-540">Boolean</span></span>|<span data-ttu-id="b8af8-541">設定アプリへのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-541">Indicates whether or not to block access to Settings app.</span></span>|
|<span data-ttu-id="b8af8-542">settingsBlockSystemPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-542">settingsBlockSystemPage</span></span>|<span data-ttu-id="b8af8-543">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-543">Boolean</span></span>|<span data-ttu-id="b8af8-544">設定アプリ内の [システム] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-544">Indicates whether or not to block access to System in Settings app.</span></span>|
|<span data-ttu-id="b8af8-545">settingsBlockDevicesPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-545">settingsBlockDevicesPage</span></span>|<span data-ttu-id="b8af8-546">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-546">Boolean</span></span>|<span data-ttu-id="b8af8-547">設定アプリ内の [デバイス] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-547">Indicates whether or not to block access to Devices in Settings app.</span></span>|
|<span data-ttu-id="b8af8-548">settingsBlockNetworkInternetPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-548">settingsBlockNetworkInternetPage</span></span>|<span data-ttu-id="b8af8-549">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-549">Boolean</span></span>|<span data-ttu-id="b8af8-550">設定アプリ内の [ネットワークとインターネット] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-550">Indicates whether or not to block access to Network & Internet in Settings app.</span></span>|
|<span data-ttu-id="b8af8-551">settingsBlockPersonalizationPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-551">settingsBlockPersonalizationPage</span></span>|<span data-ttu-id="b8af8-552">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-552">Boolean</span></span>|<span data-ttu-id="b8af8-553">設定アプリ内の [個人用設定] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-553">Indicates whether or not to block access to Personalization in Settings app.</span></span>|
|<span data-ttu-id="b8af8-554">settingsBlockAccountsPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-554">settingsBlockAccountsPage</span></span>|<span data-ttu-id="b8af8-555">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-555">Boolean</span></span>|<span data-ttu-id="b8af8-556">設定アプリ内の [アカウント] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-556">Indicates whether or not to block access to Accounts in Settings app.</span></span>|
|<span data-ttu-id="b8af8-557">settingsBlockTimeLanguagePage</span><span class="sxs-lookup"><span data-stu-id="b8af8-557">settingsBlockTimeLanguagePage</span></span>|<span data-ttu-id="b8af8-558">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-558">Boolean</span></span>|<span data-ttu-id="b8af8-559">設定アプリ内の [時刻と言語] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-559">Indicates whether or not to block access to Time & Language in Settings app.</span></span>|
|<span data-ttu-id="b8af8-560">settingsBlockEaseOfAccessPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-560">settingsBlockEaseOfAccessPage</span></span>|<span data-ttu-id="b8af8-561">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-561">Boolean</span></span>|<span data-ttu-id="b8af8-562">設定アプリ内の [簡単操作] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-562">Indicates whether or not to block access to Ease of Access in Settings app.</span></span>|
|<span data-ttu-id="b8af8-563">settingsBlockPrivacyPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-563">settingsBlockPrivacyPage</span></span>|<span data-ttu-id="b8af8-564">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-564">Boolean</span></span>|<span data-ttu-id="b8af8-565">設定アプリ内の [プライバシー] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-565">Indicates whether or not to block access to Privacy in Settings app.</span></span>|
|<span data-ttu-id="b8af8-566">settingsBlockUpdateSecurityPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-566">settingsBlockUpdateSecurityPage</span></span>|<span data-ttu-id="b8af8-567">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-567">Boolean</span></span>|<span data-ttu-id="b8af8-568">設定アプリ内の [更新とセキュリティ] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-568">Indicates whether or not to block access to Update & Security in Settings app.</span></span>|
|<span data-ttu-id="b8af8-569">settingsBlockAppsPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-569">settingsBlockAppsPage</span></span>|<span data-ttu-id="b8af8-570">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-570">Boolean</span></span>|<span data-ttu-id="b8af8-571">設定アプリ内の [アプリ] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-571">Indicates whether or not to block access to Apps in Settings app.</span></span>|
|<span data-ttu-id="b8af8-572">settingsBlockGamingPage</span><span class="sxs-lookup"><span data-stu-id="b8af8-572">settingsBlockGamingPage</span></span>|<span data-ttu-id="b8af8-573">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-573">Boolean</span></span>|<span data-ttu-id="b8af8-574">設定アプリ内の [ゲーム] へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-574">Indicates whether or not to block access to Gaming in Settings app.</span></span>|
|<span data-ttu-id="b8af8-575">windowsSpotlightBlockConsumerSpecificFeatures</span><span class="sxs-lookup"><span data-stu-id="b8af8-575">windowsSpotlightBlockConsumerSpecificFeatures</span></span>|<span data-ttu-id="b8af8-576">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-576">Boolean</span></span>|<span data-ttu-id="b8af8-577">通常はコンシューマー向けのエクスペリエンスを IT 管理者が禁止できるようにします。たとえば、開始時の提案、メンバーシップ通知、OOBE 後のアプリ インストール、リダイレクト タイルなどです。</span><span class="sxs-lookup"><span data-stu-id="b8af8-577">Allows IT admins to block experiences that are typically for consumers only, such as Start suggestions, Membership notifications, Post-OOBE app install and redirect tiles.</span></span>|
|<span data-ttu-id="b8af8-578">windowsSpotlightBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-578">windowsSpotlightBlocked</span></span>|<span data-ttu-id="b8af8-579">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-579">Boolean</span></span>|<span data-ttu-id="b8af8-580">IT 管理者が Windows スポットライトのすべての機能をオフにできるようにします</span><span class="sxs-lookup"><span data-stu-id="b8af8-580">Allows IT admins to turn off all Windows Spotlight features</span></span>|
|<span data-ttu-id="b8af8-581">windowsSpotlightBlockOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="b8af8-581">windowsSpotlightBlockOnActionCenter</span></span>|<span data-ttu-id="b8af8-582">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-582">Boolean</span></span>|<span data-ttu-id="b8af8-583">各 OS のクリーン インストールやアップグレードの後、またはその後も継続的に、新しい機能や変更された機能を Microsoft からユーザーに紹介することを禁止します</span><span class="sxs-lookup"><span data-stu-id="b8af8-583">Block suggestions from Microsoft that show after each OS clean install, upgrade or in an on-going basis to introduce users to what is new or changed</span></span>|
|<span data-ttu-id="b8af8-584">windowsSpotlightBlockTailoredExperiences</span><span class="sxs-lookup"><span data-stu-id="b8af8-584">windowsSpotlightBlockTailoredExperiences</span></span>|<span data-ttu-id="b8af8-585">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-585">Boolean</span></span>|<span data-ttu-id="b8af8-586">ユーザーのデバイスの使用状況に基づいて Windows スポットライトのコンテンツをカスタマイズすることを禁止します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-586">Block personalized content in Windows spotlight based on user’s device usage.</span></span>|
|<span data-ttu-id="b8af8-587">windowsSpotlightBlockThirdPartyNotifications</span><span class="sxs-lookup"><span data-stu-id="b8af8-587">windowsSpotlightBlockThirdPartyNotifications</span></span>|<span data-ttu-id="b8af8-588">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-588">Boolean</span></span>|<span data-ttu-id="b8af8-589">Windows スポットライト経由でサード パーティのコンテンツを配信することを禁止します</span><span class="sxs-lookup"><span data-stu-id="b8af8-589">Block third party content delivered via Windows Spotlight</span></span>|
|<span data-ttu-id="b8af8-590">windowsSpotlightBlockWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="b8af8-590">windowsSpotlightBlockWelcomeExperience</span></span>|<span data-ttu-id="b8af8-591">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-591">Boolean</span></span>|<span data-ttu-id="b8af8-592">Windows スポットライトからの Windows へようこそのエクスペリエンスを禁止します</span><span class="sxs-lookup"><span data-stu-id="b8af8-592">Block Windows Spotlight Windows welcome experience</span></span>|
|<span data-ttu-id="b8af8-593">windowsSpotlightBlockWindowsTips</span><span class="sxs-lookup"><span data-stu-id="b8af8-593">windowsSpotlightBlockWindowsTips</span></span>|<span data-ttu-id="b8af8-594">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-594">Boolean</span></span>|<span data-ttu-id="b8af8-595">Windows のヒントのポップアップを IT 管理者がオフにできるようにします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-595">Allows IT admins to turn off the popup of Windows Tips.</span></span>|
|<span data-ttu-id="b8af8-596">windowsSpotlightConfigureOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="b8af8-596">windowsSpotlightConfigureOnLockScreen</span></span>|<span data-ttu-id="b8af8-597">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-597">String</span></span>|<span data-ttu-id="b8af8-598">スポットライトの種類を指定します。可能な値は、`notConfigured`、`disabled`、`enabled` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-598">Specifies the type of Spotlight Possible values are: `notConfigured`, `disabled`, `enabled`.</span></span>|
|<span data-ttu-id="b8af8-599">networkProxyApplySettingsDeviceWide</span><span class="sxs-lookup"><span data-stu-id="b8af8-599">networkProxyApplySettingsDeviceWide</span></span>|<span data-ttu-id="b8af8-600">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-600">Boolean</span></span>|<span data-ttu-id="b8af8-601">オンに設定すると、プロキシの設定がデバイスのすべてのプロセスとアカウントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-601">If set, proxy settings will be applied to all processes and accounts in the device.</span></span> <span data-ttu-id="b8af8-602">それ以外の場合は、MDM に登録されているユーザー アカウントに適用されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-602">Otherwise, it will be applied to the user account that’s enrolled into MDM.</span></span>|
|<span data-ttu-id="b8af8-603">networkProxyDisableAutoDetect</span><span class="sxs-lookup"><span data-stu-id="b8af8-603">networkProxyDisableAutoDetect</span></span>|<span data-ttu-id="b8af8-604">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-604">Boolean</span></span>|<span data-ttu-id="b8af8-605">設定の自動検出を無効にします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-605">Disable automatic detection of settings.</span></span> <span data-ttu-id="b8af8-606">有効にした場合、システムはプロキシ自動構成 (PAC) スクリプトへのパスを検索します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-606">If enabled, the system will try to find the path to a proxy auto-config (PAC) script.</span></span>|
|<span data-ttu-id="b8af8-607">networkProxyAutomaticConfigurationUrl</span><span class="sxs-lookup"><span data-stu-id="b8af8-607">networkProxyAutomaticConfigurationUrl</span></span>|<span data-ttu-id="b8af8-608">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-608">String</span></span>|<span data-ttu-id="b8af8-609">使用するプロキシ自動構成 (PAC) スクリプトのアドレス。</span><span class="sxs-lookup"><span data-stu-id="b8af8-609">Address to the proxy auto-config (PAC) script you want to use.</span></span>|
|<span data-ttu-id="b8af8-610">networkProxyServer</span><span class="sxs-lookup"><span data-stu-id="b8af8-610">networkProxyServer</span></span>|[<span data-ttu-id="b8af8-611">windows10NetworkProxyServer</span><span class="sxs-lookup"><span data-stu-id="b8af8-611">windows10NetworkProxyServer</span></span>](../resources/intune_deviceconfig_windows10networkproxyserver.md)|<span data-ttu-id="b8af8-612">プロキシ サーバーの設定を手動で指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-612">Specifies manual proxy server settings.</span></span>|
|<span data-ttu-id="b8af8-613">accountsBlockAddingNonMicrosoftAccountEmail</span><span class="sxs-lookup"><span data-stu-id="b8af8-613">accountsBlockAddingNonMicrosoftAccountEmail</span></span>|<span data-ttu-id="b8af8-614">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-614">Boolean</span></span>|<span data-ttu-id="b8af8-615">Microsoft アカウントに関連付けられていない電子メール アカウントをユーザーがデバイスに追加できないようにするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-615">Indicates whether or not to Block the user from adding email accounts to the device that are not associated with a Microsoft account.</span></span>|
|<span data-ttu-id="b8af8-616">antiTheftModeBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-616">antiTheftModeBlocked</span></span>|<span data-ttu-id="b8af8-617">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-617">Boolean</span></span>|<span data-ttu-id="b8af8-618">ユーザーが盗難防止モードの設定を選択することを禁止するかどうかを示します (Windows 10 Mobile のみ)。</span><span class="sxs-lookup"><span data-stu-id="b8af8-618">Indicates whether or not to block the user from selecting an AntiTheft mode preference (Windows 10 Mobile only).</span></span>|
|<span data-ttu-id="b8af8-619">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-619">bluetoothBlocked</span></span>|<span data-ttu-id="b8af8-620">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-620">Boolean</span></span>|<span data-ttu-id="b8af8-621">ユーザーが Bluetooth を使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-621">Whether or not to Block the user from using bluetooth.</span></span>|
|<span data-ttu-id="b8af8-622">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-622">cameraBlocked</span></span>|<span data-ttu-id="b8af8-623">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-623">Boolean</span></span>|<span data-ttu-id="b8af8-624">ユーザーがデバイスのカメラにアクセスすることを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-624">Whether or not to Block the user from accessing the camera of the device.</span></span>|
|<span data-ttu-id="b8af8-625">connectedDevicesServiceBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-625">connectedDevicesServiceBlocked</span></span>|<span data-ttu-id="b8af8-626">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-626">Boolean</span></span>|<span data-ttu-id="b8af8-627">他のデバイスの検出と接続、リモート メッセージング、リモート アプリ セッション、その他のデバイス間エクスペリエンスを可能にする、接続されているデバイスのサービスを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-627">Whether or not to block Connected Devices Service which enables discovery and connection to other devices, remote messaging, remote app sessions and other cross-device experiences.</span></span>|
|<span data-ttu-id="b8af8-628">certificatesBlockManualRootCertificateInstallation</span><span class="sxs-lookup"><span data-stu-id="b8af8-628">certificatesBlockManualRootCertificateInstallation</span></span>|<span data-ttu-id="b8af8-629">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-629">Boolean</span></span>|<span data-ttu-id="b8af8-630">ユーザーが手動でルート証明書をインストールすることを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-630">Whether or not to Block the user from doing manual root certificate installation.</span></span>|
|<span data-ttu-id="b8af8-631">copyPasteBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-631">copyPasteBlocked</span></span>|<span data-ttu-id="b8af8-632">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-632">Boolean</span></span>|<span data-ttu-id="b8af8-633">ユーザーがコピーと貼り付けを使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-633">Whether or not to Block the user from using copy paste.</span></span>|
|<span data-ttu-id="b8af8-634">cortanaBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-634">cortanaBlocked</span></span>|<span data-ttu-id="b8af8-635">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-635">Boolean</span></span>|<span data-ttu-id="b8af8-636">ユーザーが Cortana を使用することを禁止するかどうか。</span><span class="sxs-lookup"><span data-stu-id="b8af8-636">Whether or not to Block the user from using Cortana.</span></span>|
|<span data-ttu-id="b8af8-637">deviceManagementBlockFactoryResetOnMobile</span><span class="sxs-lookup"><span data-stu-id="b8af8-637">deviceManagementBlockFactoryResetOnMobile</span></span>|<span data-ttu-id="b8af8-638">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-638">Boolean</span></span>|<span data-ttu-id="b8af8-639">ユーザーが携帯電話をリセットすることを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-639">Indicates whether or not to Block the user from resetting their phone.</span></span>|
|<span data-ttu-id="b8af8-640">deviceManagementBlockManualUnenroll</span><span class="sxs-lookup"><span data-stu-id="b8af8-640">deviceManagementBlockManualUnenroll</span></span>|<span data-ttu-id="b8af8-641">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-641">Boolean</span></span>|<span data-ttu-id="b8af8-642">ユーザーがデバイス管理から手動で登録解除を行うことを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-642">Indicates whether or not to Block the user from doing manual un-enrollment from device management.</span></span>|
|<span data-ttu-id="b8af8-643">safeSearchFilter</span><span class="sxs-lookup"><span data-stu-id="b8af8-643">safeSearchFilter</span></span>|<span data-ttu-id="b8af8-644">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-644">String</span></span>|<span data-ttu-id="b8af8-645">セーフ サーチに必要なフィルター レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-645">Specifies what filter level of safe search is required.</span></span> <span data-ttu-id="b8af8-646">可能な値は、`userDefined`、`strict`、`moderate` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-646">Possible values are: `userDefined`, `strict`, `moderate`.</span></span>|
|<span data-ttu-id="b8af8-647">edgeBlockPopups</span><span class="sxs-lookup"><span data-stu-id="b8af8-647">edgeBlockPopups</span></span>|<span data-ttu-id="b8af8-648">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-648">Boolean</span></span>|<span data-ttu-id="b8af8-649">ポップアップをブロックするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-649">Indicates whether or not to block popups.</span></span>|
|<span data-ttu-id="b8af8-650">edgeBlockSearchSuggestions</span><span class="sxs-lookup"><span data-stu-id="b8af8-650">edgeBlockSearchSuggestions</span></span>|<span data-ttu-id="b8af8-651">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-651">Boolean</span></span>|<span data-ttu-id="b8af8-652">ユーザーがアドレス バーで検索候補を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-652">Indicates whether or not to Block the user from using the search suggestions in the address bar.</span></span>|
|<span data-ttu-id="b8af8-653">edgeBlockSendingIntranetTrafficToInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="b8af8-653">edgeBlockSendingIntranetTrafficToInternetExplorer</span></span>|<span data-ttu-id="b8af8-654">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-654">Boolean</span></span>|<span data-ttu-id="b8af8-655">ユーザーが Edge から Internet Explorer にイントラネット トラフィックを送信することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-655">Indicates whether or not to Block the user from sending Intranet traffic to Internet Explorer from Edge.</span></span>|
|<span data-ttu-id="b8af8-656">edgeRequireSmartScreen</span><span class="sxs-lookup"><span data-stu-id="b8af8-656">edgeRequireSmartScreen</span></span>|<span data-ttu-id="b8af8-657">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-657">Boolean</span></span>|<span data-ttu-id="b8af8-658">スマート スクリーン フィルターの使用をユーザーに要求するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-658">Indicates whether or not to Require the user to use the smart screen filter.</span></span>|
|<span data-ttu-id="b8af8-659">edgeEnterpriseModeSiteListLocation</span><span class="sxs-lookup"><span data-stu-id="b8af8-659">edgeEnterpriseModeSiteListLocation</span></span>|<span data-ttu-id="b8af8-660">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-660">String</span></span>|<span data-ttu-id="b8af8-661">エンタープライズ モードのサイト リストの場所を示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-661">Indicates the enterprise mode site list location.</span></span> <span data-ttu-id="b8af8-662">ローカル ファイル、ローカル ネットワーク、http の場所が該当します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-662">Could be a local file, local network or http location.</span></span>|
|<span data-ttu-id="b8af8-663">edgeFirstRunUrl</span><span class="sxs-lookup"><span data-stu-id="b8af8-663">edgeFirstRunUrl</span></span>|<span data-ttu-id="b8af8-664">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-664">String</span></span>|<span data-ttu-id="b8af8-665">Edge ブラウザーを初めて開いたときに最初に実行される URL です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-665">The first run URL for when Edge browser is opened for the first time.</span></span>|
|<span data-ttu-id="b8af8-666">edgeSearchEngine</span><span class="sxs-lookup"><span data-stu-id="b8af8-666">edgeSearchEngine</span></span>|[<span data-ttu-id="b8af8-667">edgeSearchEngineBase</span><span class="sxs-lookup"><span data-stu-id="b8af8-667">edgeSearchEngineBase</span></span>](../resources/intune_deviceconfig_edgesearchenginebase.md)|<span data-ttu-id="b8af8-668">IT 管理者が MDM 制御デバイス用の既定の検索エンジンを設定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-668">Allows IT admins to set a default search engine for MDM-Controlled devices.</span></span> <span data-ttu-id="b8af8-669">AllowSearchEngineCustomization ポリシーが設定されていない場合、ユーザーは上書きして既定の検索エンジンを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-669">Users can override this and change their default search engine provided the AllowSearchEngineCustomization policy is not set.</span></span>|
|<span data-ttu-id="b8af8-670">edgeHomepageUrls</span><span class="sxs-lookup"><span data-stu-id="b8af8-670">edgeHomepageUrls</span></span>|<span data-ttu-id="b8af8-671">String コレクション</span><span class="sxs-lookup"><span data-stu-id="b8af8-671">String collection</span></span>|<span data-ttu-id="b8af8-672">MDM に登録されているデバイスの Edge ブラウザーに表示されるホームページの URL の一覧です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-672">The list of URLs for homepages shodwn on MDM-enrolled devices on Edge browser.</span></span>|
|<span data-ttu-id="b8af8-673">edgeBlockAccessToAboutFlags</span><span class="sxs-lookup"><span data-stu-id="b8af8-673">edgeBlockAccessToAboutFlags</span></span>|<span data-ttu-id="b8af8-674">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-674">Boolean</span></span>|<span data-ttu-id="b8af8-675">Edge ブラウザーの about:flags へのアクセスを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-675">Indicates whether or not to prevent access to about flags on Edge browser.</span></span>|
|<span data-ttu-id="b8af8-676">smartScreenBlockPromptOverride</span><span class="sxs-lookup"><span data-stu-id="b8af8-676">smartScreenBlockPromptOverride</span></span>|<span data-ttu-id="b8af8-677">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-677">Boolean</span></span>|<span data-ttu-id="b8af8-678">悪意のある Web サイトの可能性があるサイトに関する SmartScreen フィルターの警告をユーザーが無視できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-678">Indicates whether or not users can override SmartScreen Filter warnings about potentially malicious websites.</span></span>|
|<span data-ttu-id="b8af8-679">smartScreenBlockPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="b8af8-679">smartScreenBlockPromptOverrideForFiles</span></span>|<span data-ttu-id="b8af8-680">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-680">Boolean</span></span>|<span data-ttu-id="b8af8-681">未検証のファイルのダウンロードに関する SmartScreen フィルターの警告をユーザーが無視できるかどうかを示します</span><span class="sxs-lookup"><span data-stu-id="b8af8-681">Indicates whether or not users can override the SmartScreen Filter warnings about downloading unverified files</span></span>|
|<span data-ttu-id="b8af8-682">webRtcBlockLocalhostIpAddress</span><span class="sxs-lookup"><span data-stu-id="b8af8-682">webRtcBlockLocalhostIpAddress</span></span>|<span data-ttu-id="b8af8-683">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-683">Boolean</span></span>|<span data-ttu-id="b8af8-684">WebRTC を使用して通話を発信しているときにユーザーのローカル ホストの IP アドレスが表示されるかどうかを示します</span><span class="sxs-lookup"><span data-stu-id="b8af8-684">Indicates whether or not user's localhost IP address is displayed while making phone calls using the WebRTC</span></span>|
|<span data-ttu-id="b8af8-685">internetSharingBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-685">internetSharingBlocked</span></span>|<span data-ttu-id="b8af8-686">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-686">Boolean</span></span>|<span data-ttu-id="b8af8-687">ユーザーがインターネット共有を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-687">Indicates whether or not to Block the user from using internet sharing.</span></span>|
|<span data-ttu-id="b8af8-688">settingsBlockAddProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="b8af8-688">settingsBlockAddProvisioningPackage</span></span>|<span data-ttu-id="b8af8-689">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-689">Boolean</span></span>|<span data-ttu-id="b8af8-690">ユーザーがプロビジョニング パッケージをインストールすることを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-690">Indicates whether or not to block the user from installing provisioning packages.</span></span>|
|<span data-ttu-id="b8af8-691">settingsBlockRemoveProvisioningPackage</span><span class="sxs-lookup"><span data-stu-id="b8af8-691">settingsBlockRemoveProvisioningPackage</span></span>|<span data-ttu-id="b8af8-692">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-692">Boolean</span></span>|<span data-ttu-id="b8af8-693">ランタイム構成エージェントがプロビジョニング パッケージを削除することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-693">Indicates whether or not to block the runtime configuration agent from removing provisioning packages.</span></span>|
|<span data-ttu-id="b8af8-694">settingsBlockChangeSystemTime</span><span class="sxs-lookup"><span data-stu-id="b8af8-694">settingsBlockChangeSystemTime</span></span>|<span data-ttu-id="b8af8-695">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-695">Boolean</span></span>|<span data-ttu-id="b8af8-696">ユーザーが日付と時刻の設定を変更することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-696">Indicates whether or not to block the user from changing date and time settings.</span></span>|
|<span data-ttu-id="b8af8-697">settingsBlockEditDeviceName</span><span class="sxs-lookup"><span data-stu-id="b8af8-697">settingsBlockEditDeviceName</span></span>|<span data-ttu-id="b8af8-698">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-698">Boolean</span></span>|<span data-ttu-id="b8af8-699">ユーザーがデバイス名を編集することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-699">Indicates whether or not to block the user from editing the device name.</span></span>|
|<span data-ttu-id="b8af8-700">settingsBlockChangeRegion</span><span class="sxs-lookup"><span data-stu-id="b8af8-700">settingsBlockChangeRegion</span></span>|<span data-ttu-id="b8af8-701">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-701">Boolean</span></span>|<span data-ttu-id="b8af8-702">ユーザーがリージョン設定を変更することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-702">Indicates whether or not to block the user from changing the region settings.</span></span>|
|<span data-ttu-id="b8af8-703">settingsBlockChangeLanguage</span><span class="sxs-lookup"><span data-stu-id="b8af8-703">settingsBlockChangeLanguage</span></span>|<span data-ttu-id="b8af8-704">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-704">Boolean</span></span>|<span data-ttu-id="b8af8-705">ユーザーが言語の設定を変更することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-705">Indicates whether or not to block the user from changing the language settings.</span></span>|
|<span data-ttu-id="b8af8-706">settingsBlockChangePowerSleep</span><span class="sxs-lookup"><span data-stu-id="b8af8-706">settingsBlockChangePowerSleep</span></span>|<span data-ttu-id="b8af8-707">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-707">Boolean</span></span>|<span data-ttu-id="b8af8-708">ユーザーが電源とスリープの設定を変更することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-708">Indicates whether or not to block the user from changing power and sleep settings.</span></span>|
|<span data-ttu-id="b8af8-709">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-709">locationServicesBlocked</span></span>|<span data-ttu-id="b8af8-710">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-710">Boolean</span></span>|<span data-ttu-id="b8af8-711">ユーザーが位置情報サービスを使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-711">Indicates whether or not to Block the user from location services.</span></span>|
|<span data-ttu-id="b8af8-712">microsoftAccountBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-712">microsoftAccountBlocked</span></span>|<span data-ttu-id="b8af8-713">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-713">Boolean</span></span>|<span data-ttu-id="b8af8-714">Microsoft アカウントを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-714">Indicates whether or not to Block a Microsoft account.</span></span>|
|<span data-ttu-id="b8af8-715">microsoftAccountBlockSettingsSync</span><span class="sxs-lookup"><span data-stu-id="b8af8-715">microsoftAccountBlockSettingsSync</span></span>|<span data-ttu-id="b8af8-716">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-716">Boolean</span></span>|<span data-ttu-id="b8af8-717">Microsoft アカウントの設定の同期を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-717">Indicates whether or not to Block Microsoft account settings sync.</span></span>|
|<span data-ttu-id="b8af8-718">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-718">nfcBlocked</span></span>|<span data-ttu-id="b8af8-719">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-719">Boolean</span></span>|<span data-ttu-id="b8af8-720">ユーザーが近距離無線通信を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-720">Indicates whether or not to Block the user from using near field communication.</span></span>|
|<span data-ttu-id="b8af8-721">resetProtectionModeBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-721">resetProtectionModeBlocked</span></span>|<span data-ttu-id="b8af8-722">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-722">Boolean</span></span>|<span data-ttu-id="b8af8-723">ユーザーが保護モードをリセットすることを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-723">Indicates whether or not to Block the user from reset protection mode.</span></span>|
|<span data-ttu-id="b8af8-724">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-724">screenCaptureBlocked</span></span>|<span data-ttu-id="b8af8-725">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-725">Boolean</span></span>|<span data-ttu-id="b8af8-726">ユーザーがスクリーンショットを撮ることを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-726">Indicates whether or not to Block the user from taking Screenshots.</span></span>|
|<span data-ttu-id="b8af8-727">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="b8af8-727">storageBlockRemovableStorage</span></span>|<span data-ttu-id="b8af8-728">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-728">Boolean</span></span>|<span data-ttu-id="b8af8-729">ユーザーがリムーバブル記憶域を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-729">Indicates whether or not to Block the user from using removable storage.</span></span>|
|<span data-ttu-id="b8af8-730">storageRequireMobileDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="b8af8-730">storageRequireMobileDeviceEncryption</span></span>|<span data-ttu-id="b8af8-731">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-731">Boolean</span></span>|<span data-ttu-id="b8af8-732">モバイル デバイスでの暗号化が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-732">Indicating whether or not to require encryption on a mobile device.</span></span>|
|<span data-ttu-id="b8af8-733">usbBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-733">usbBlocked</span></span>|<span data-ttu-id="b8af8-734">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-734">Boolean</span></span>|<span data-ttu-id="b8af8-735">ユーザーが USB 接続を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-735">Indicates whether or not to Block the user from USB connection.</span></span>|
|<span data-ttu-id="b8af8-736">voiceRecordingBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-736">voiceRecordingBlocked</span></span>|<span data-ttu-id="b8af8-737">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-737">Boolean</span></span>|<span data-ttu-id="b8af8-738">ユーザーが音声録音を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-738">Indicates whether or not to Block the user from voice recording.</span></span>|
|<span data-ttu-id="b8af8-739">wiFiBlockAutomaticConnectHotspots</span><span class="sxs-lookup"><span data-stu-id="b8af8-739">wiFiBlockAutomaticConnectHotspots</span></span>|<span data-ttu-id="b8af8-740">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-740">Boolean</span></span>|<span data-ttu-id="b8af8-741">Wi-Fi ホットスポットへの自動接続を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-741">Indicating whether or not to block automatically connecting to Wi-Fi hotspots.</span></span> <span data-ttu-id="b8af8-742">Wi-Fi がブロックされていれば、この値は関係ありません。</span><span class="sxs-lookup"><span data-stu-id="b8af8-742">Has no impact if Wi-Fi is blocked.</span></span>|
|<span data-ttu-id="b8af8-743">wiFiBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-743">wiFiBlocked</span></span>|<span data-ttu-id="b8af8-744">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-744">Boolean</span></span>|<span data-ttu-id="b8af8-745">ユーザーが Wi-Fi を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-745">Indicates whether or not to Block the user from using Wi-Fi.</span></span>|
|<span data-ttu-id="b8af8-746">wiFiBlockManualConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8af8-746">wiFiBlockManualConfiguration</span></span>|<span data-ttu-id="b8af8-747">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-747">Boolean</span></span>|<span data-ttu-id="b8af8-748">ユーザーが Wi-Fi の手動構成を使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-748">Indicates whether or not to Block the user from using Wi-Fi manual configuration.</span></span>|
|<span data-ttu-id="b8af8-749">wiFiScanInterval</span><span class="sxs-lookup"><span data-stu-id="b8af8-749">wiFiScanInterval</span></span>|<span data-ttu-id="b8af8-750">Int32</span><span class="sxs-lookup"><span data-stu-id="b8af8-750">Int32</span></span>|<span data-ttu-id="b8af8-751">Wi-Fi ネットワークに対するデバイス スキャンの頻度を指定します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-751">Specify how often devices scan for Wi-Fi networks.</span></span> <span data-ttu-id="b8af8-752">サポートされている値は 1 から 500 まで、既定値は 100、500 は最低頻度です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-752">Supported values are 1-500, where 100 = default, and 500 = low frequency.</span></span> <span data-ttu-id="b8af8-753">有効な値は 1 から 500 までです</span><span class="sxs-lookup"><span data-stu-id="b8af8-753">Valid values are 1 to 500. The default value is 75.</span></span>|
|<span data-ttu-id="b8af8-754">wirelessDisplayBlockProjectionToThisDevice</span><span class="sxs-lookup"><span data-stu-id="b8af8-754">wirelessDisplayBlockProjectionToThisDevice</span></span>|<span data-ttu-id="b8af8-755">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-755">Boolean</span></span>|<span data-ttu-id="b8af8-756">他のデバイスがこの PC をプロジェクター用に検出することを許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-756">Indicates whether or not to allow other devices from discovering this PC for projection.</span></span>|
|<span data-ttu-id="b8af8-757">wirelessDisplayBlockUserInputFromReceiver</span><span class="sxs-lookup"><span data-stu-id="b8af8-757">wirelessDisplayBlockUserInputFromReceiver</span></span>|<span data-ttu-id="b8af8-758">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-758">Boolean</span></span>|<span data-ttu-id="b8af8-759">ワイヤレス ディスプレイ レシーバーからのユーザー入力を許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-759">Indicates whether or not to allow user input from wireless display receiver.</span></span>|
|<span data-ttu-id="b8af8-760">wirelessDisplayRequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="b8af8-760">wirelessDisplayRequirePinForPairing</span></span>|<span data-ttu-id="b8af8-761">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-761">Boolean</span></span>|<span data-ttu-id="b8af8-762">新しいデバイスがペアリングを開始するときに PIN が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-762">Indicates whether or not to require a PIN for new devices to initiate pairing.</span></span>|
|<span data-ttu-id="b8af8-763">windowsStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-763">windowsStoreBlocked</span></span>|<span data-ttu-id="b8af8-764">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-764">Boolean</span></span>|<span data-ttu-id="b8af8-765">ユーザーが Windows ストアを使用することを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-765">Indicates whether or not to Block the user from using the Windows store.</span></span>|
|<span data-ttu-id="b8af8-766">appsAllowTrustedAppsSideloading</span><span class="sxs-lookup"><span data-stu-id="b8af8-766">appsAllowTrustedAppsSideloading</span></span>|<span data-ttu-id="b8af8-767">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-767">String</span></span>|<span data-ttu-id="b8af8-768">信頼された証明書で署名した AppX パッケージからアプリをサイドローディングできるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-768">Indicates whether apps from AppX packages signed with a trusted certificate can be side loaded.</span></span> <span data-ttu-id="b8af8-769">可能な値は、`notConfigured`、`blocked`、`allowed` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-769">Possible values are: `notConfigured`, `blocked`, `allowed`.</span></span>|
|<span data-ttu-id="b8af8-770">windowsStoreBlockAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="b8af8-770">windowsStoreBlockAutoUpdate</span></span>|<span data-ttu-id="b8af8-771">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-771">Boolean</span></span>|<span data-ttu-id="b8af8-772">Windows ストアからのアプリの自動更新を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-772">Indicates whether or not to block automatic update of apps from Windows Store.</span></span>|
|<span data-ttu-id="b8af8-773">developerUnlockSetting</span><span class="sxs-lookup"><span data-stu-id="b8af8-773">developerUnlockSetting</span></span>|<span data-ttu-id="b8af8-774">String</span><span class="sxs-lookup"><span data-stu-id="b8af8-774">String</span></span>|<span data-ttu-id="b8af8-775">開発者によるロック解除を許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-775">Indicates whether or not to allow developer unlock.</span></span> <span data-ttu-id="b8af8-776">可能な値は、`notConfigured`、`blocked`、`allowed` です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-776">Possible values are: `notConfigured`, `blocked`, `allowed`.</span></span>|
|<span data-ttu-id="b8af8-777">sharedUserAppDataAllowed</span><span class="sxs-lookup"><span data-stu-id="b8af8-777">sharedUserAppDataAllowed</span></span>|<span data-ttu-id="b8af8-778">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-778">Boolean</span></span>|<span data-ttu-id="b8af8-779">同じアプリの複数のユーザーによるデータ共有を禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-779">Indicates whether or not to block multiple users of the same app to share data.</span></span>|
|<span data-ttu-id="b8af8-780">appsBlockWindowsStoreOriginatedApps</span><span class="sxs-lookup"><span data-stu-id="b8af8-780">appsBlockWindowsStoreOriginatedApps</span></span>|<span data-ttu-id="b8af8-781">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-781">Boolean</span></span>|<span data-ttu-id="b8af8-782">プレインストールまたはダウンロードによって取得したすべての Windows ストア アプリの起動を無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-782">Indicates whether or not to disable the launch of all apps from Windows Store that came pre-installed or were downloaded.</span></span>|
|<span data-ttu-id="b8af8-783">windowsStoreEnablePrivateStoreOnly</span><span class="sxs-lookup"><span data-stu-id="b8af8-783">windowsStoreEnablePrivateStoreOnly</span></span>|<span data-ttu-id="b8af8-784">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-784">Boolean</span></span>|<span data-ttu-id="b8af8-785">プライベート ストアのみを有効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-785">Indicates whether or not to enable Private Store Only.</span></span>|
|<span data-ttu-id="b8af8-786">storageRestrictAppDataToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="b8af8-786">storageRestrictAppDataToSystemVolume</span></span>|<span data-ttu-id="b8af8-787">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-787">Boolean</span></span>|<span data-ttu-id="b8af8-788">アプリケーションのデータがシステム ドライブに制限されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-788">Indicates whether application data is restricted to the system drive.</span></span>|
|<span data-ttu-id="b8af8-789">storageRestrictAppInstallToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="b8af8-789">storageRestrictAppInstallToSystemVolume</span></span>|<span data-ttu-id="b8af8-790">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-790">Boolean</span></span>|<span data-ttu-id="b8af8-791">アプリケーションのインストールがシステム ドライブに制限されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-791">Indicates whether the installation of applications is restricted to the system drive.</span></span>|
|<span data-ttu-id="b8af8-792">gameDvrBlocked</span><span class="sxs-lookup"><span data-stu-id="b8af8-792">gameDvrBlocked</span></span>|<span data-ttu-id="b8af8-793">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-793">Boolean</span></span>|<span data-ttu-id="b8af8-794">DVR とブロードキャストを禁止するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-794">Indicates whether or not to block DVR and broadcasting.</span></span>|
|<span data-ttu-id="b8af8-795">experienceBlockDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="b8af8-795">experienceBlockDeviceDiscovery</span></span>|<span data-ttu-id="b8af8-796">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-796">Boolean</span></span>|<span data-ttu-id="b8af8-797">デバイス検出 UX を有効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-797">Indicates whether or not to enable device discovery UX.</span></span>|
|<span data-ttu-id="b8af8-798">experienceBlockErrorDialogWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="b8af8-798">experienceBlockErrorDialogWhenNoSIM</span></span>|<span data-ttu-id="b8af8-799">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-799">Boolean</span></span>|<span data-ttu-id="b8af8-800">SIM カードが検出されない場合にエラー ダイアログを表示することを許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-800">Indicates whether or not to allow the error dialog from displaying if no SIM card is detected.</span></span>|
|<span data-ttu-id="b8af8-801">experienceBlockTaskSwitcher</span><span class="sxs-lookup"><span data-stu-id="b8af8-801">experienceBlockTaskSwitcher</span></span>|<span data-ttu-id="b8af8-802">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-802">Boolean</span></span>|<span data-ttu-id="b8af8-803">デバイスでのタスクの切り替えを有効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-803">Indicates whether or not to enable task switching on the device.</span></span>|
|<span data-ttu-id="b8af8-804">logonBlockFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="b8af8-804">logonBlockFastUserSwitching</span></span>|<span data-ttu-id="b8af8-805">Boolean</span><span class="sxs-lookup"><span data-stu-id="b8af8-805">Boolean</span></span>|<span data-ttu-id="b8af8-806">同時にログオンしているユーザー間での切り替えをログオフなしで迅速に行う機能を無効にします。</span><span class="sxs-lookup"><span data-stu-id="b8af8-806">Disables the ability to quickly switch between users that are logged on simultaneously without logging off.</span></span>|



## <a name="response"></a><span data-ttu-id="b8af8-807">応答</span><span class="sxs-lookup"><span data-stu-id="b8af8-807">Response</span></span>
<span data-ttu-id="b8af8-808">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [windows10GeneralConfiguration](../resources/intune_deviceconfig_windows10generalconfiguration.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="b8af8-808">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_deviceconfig_windows10generalconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8af8-809">例</span><span class="sxs-lookup"><span data-stu-id="b8af8-809">Example</span></span>
### <a name="request"></a><span data-ttu-id="b8af8-810">要求</span><span class="sxs-lookup"><span data-stu-id="b8af8-810">Request</span></span>
<span data-ttu-id="b8af8-811">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="b8af8-811">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 9767

{
  "@odata.type": "#microsoft.graph.windows10GeneralConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enterpriseCloudPrintDiscoveryEndPoint": "Enterprise Cloud Print Discovery End Point value",
  "enterpriseCloudPrintOAuthAuthority": "Enterprise Cloud Print OAuth Authority value",
  "enterpriseCloudPrintOAuthClientIdentifier": "Enterprise Cloud Print OAuth Client Identifier value",
  "enterpriseCloudPrintResourceIdentifier": "Enterprise Cloud Print Resource Identifier value",
  "enterpriseCloudPrintDiscoveryMaxLimit": 5,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "Enterprise Cloud Print Mopria Discovery Resource Identifier value",
  "searchBlockDiacritics": true,
  "searchDisableAutoLanguageDetection": true,
  "searchDisableIndexingEncryptedItems": true,
  "searchEnableRemoteQueries": true,
  "searchDisableIndexerBackoff": true,
  "searchDisableIndexingRemovableDrive": true,
  "searchEnableAutomaticIndexSizeManangement": true,
  "diagnosticsDataSubmissionMode": "none",
  "oneDriveDisableFileSync": true,
  "smartScreenEnableAppInstallControl": true,
  "personalizationDesktopImageUrl": "https://example.com/personalizationDesktopImageUrl/",
  "personalizationLockScreenImageUrl": "https://example.com/personalizationLockScreenImageUrl/",
  "bluetoothAllowedServices": [
    "Bluetooth Allowed Services value"
  ],
  "bluetoothBlockAdvertising": true,
  "bluetoothBlockDiscoverableMode": true,
  "bluetoothBlockPrePairing": true,
  "edgeBlockAutofill": true,
  "edgeBlocked": true,
  "edgeCookiePolicy": "allow",
  "edgeBlockDeveloperTools": true,
  "edgeBlockSendingDoNotTrackHeader": true,
  "edgeBlockExtensions": true,
  "edgeBlockInPrivateBrowsing": true,
  "edgeBlockJavaScript": true,
  "edgeBlockPasswordManager": true,
  "edgeBlockAddressBarDropdown": true,
  "edgeBlockCompatibilityList": true,
  "edgeClearBrowsingDataOnExit": true,
  "edgeAllowStartPagesModification": true,
  "edgeDisableFirstRunPage": true,
  "edgeBlockLiveTileDataCollection": true,
  "edgeSyncFavoritesWithInternetExplorer": true,
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
  "defenderBlockEndUserAccess": true,
  "defenderDaysBeforeDeletingQuarantinedMalware": 12,
  "defenderDetectedMalwareActions": {
    "@odata.type": "microsoft.graph.defenderDetectedMalwareActions",
    "lowSeverity": "clean",
    "moderateSeverity": "clean",
    "highSeverity": "clean",
    "severeSeverity": "clean"
  },
  "defenderSystemScanSchedule": "everyday",
  "defenderFilesAndFoldersToExclude": [
    "Defender Files And Folders To Exclude value"
  ],
  "defenderFileExtensionsToExclude": [
    "Defender File Extensions To Exclude value"
  ],
  "defenderScanMaxCpu": 2,
  "defenderMonitorFileActivity": "disable",
  "defenderProcessesToExclude": [
    "Defender Processes To Exclude value"
  ],
  "defenderPromptForSampleSubmission": "alwaysPrompt",
  "defenderRequireBehaviorMonitoring": true,
  "defenderRequireCloudProtection": true,
  "defenderRequireNetworkInspectionSystem": true,
  "defenderRequireRealTimeMonitoring": true,
  "defenderScanArchiveFiles": true,
  "defenderScanDownloads": true,
  "defenderScanNetworkFiles": true,
  "defenderScanIncomingMail": true,
  "defenderScanMappedNetworkDrivesDuringFullScan": true,
  "defenderScanRemovableDrivesDuringFullScan": true,
  "defenderScanScriptsLoadedInInternetExplorer": true,
  "defenderSignatureUpdateIntervalInHours": 6,
  "defenderScanType": "disabled",
  "defenderScheduledScanTime": "11:59:10.9990000",
  "defenderScheduledQuickScanTime": "11:58:49.3840000",
  "defenderCloudBlockLevel": "high",
  "lockScreenAllowTimeoutConfiguration": true,
  "lockScreenBlockActionCenterNotifications": true,
  "lockScreenBlockCortana": true,
  "lockScreenBlockToastNotifications": true,
  "lockScreenTimeoutInSeconds": 10,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "passwordRequireWhenResumeFromIdleState": true,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "privacyAdvertisingId": "blocked",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
  "startBlockUnpinningAppsFromTaskbar": true,
  "startMenuAppListVisibility": "collapse",
  "startMenuHideChangeAccountSettings": true,
  "startMenuHideFrequentlyUsedApps": true,
  "startMenuHideHibernate": true,
  "startMenuHideLock": true,
  "startMenuHidePowerButton": true,
  "startMenuHideRecentJumpLists": true,
  "startMenuHideRecentlyAddedApps": true,
  "startMenuHideRestartOptions": true,
  "startMenuHideShutDown": true,
  "startMenuHideSignOut": true,
  "startMenuHideSleep": true,
  "startMenuHideSwitchAccount": true,
  "startMenuHideUserTile": true,
  "startMenuLayoutEdgeAssetsXml": "c3RhcnRNZW51TGF5b3V0RWRnZUFzc2V0c1htbA==",
  "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s",
  "startMenuMode": "fullScreen",
  "startMenuPinnedFolderDocuments": "hide",
  "startMenuPinnedFolderDownloads": "hide",
  "startMenuPinnedFolderFileExplorer": "hide",
  "startMenuPinnedFolderHomeGroup": "hide",
  "startMenuPinnedFolderMusic": "hide",
  "startMenuPinnedFolderNetwork": "hide",
  "startMenuPinnedFolderPersonalFolder": "hide",
  "startMenuPinnedFolderPictures": "hide",
  "startMenuPinnedFolderSettings": "hide",
  "startMenuPinnedFolderVideos": "hide",
  "settingsBlockSettingsApp": true,
  "settingsBlockSystemPage": true,
  "settingsBlockDevicesPage": true,
  "settingsBlockNetworkInternetPage": true,
  "settingsBlockPersonalizationPage": true,
  "settingsBlockAccountsPage": true,
  "settingsBlockTimeLanguagePage": true,
  "settingsBlockEaseOfAccessPage": true,
  "settingsBlockPrivacyPage": true,
  "settingsBlockUpdateSecurityPage": true,
  "settingsBlockAppsPage": true,
  "settingsBlockGamingPage": true,
  "windowsSpotlightBlockConsumerSpecificFeatures": true,
  "windowsSpotlightBlocked": true,
  "windowsSpotlightBlockOnActionCenter": true,
  "windowsSpotlightBlockTailoredExperiences": true,
  "windowsSpotlightBlockThirdPartyNotifications": true,
  "windowsSpotlightBlockWelcomeExperience": true,
  "windowsSpotlightBlockWindowsTips": true,
  "windowsSpotlightConfigureOnLockScreen": "disabled",
  "networkProxyApplySettingsDeviceWide": true,
  "networkProxyDisableAutoDetect": true,
  "networkProxyAutomaticConfigurationUrl": "https://example.com/networkProxyAutomaticConfigurationUrl/",
  "networkProxyServer": {
    "@odata.type": "microsoft.graph.windows10NetworkProxyServer",
    "address": "Address value",
    "exceptions": [
      "Exceptions value"
    ],
    "useForLocalAddresses": true
  },
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "antiTheftModeBlocked": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "connectedDevicesServiceBlocked": true,
  "certificatesBlockManualRootCertificateInstallation": true,
  "copyPasteBlocked": true,
  "cortanaBlocked": true,
  "deviceManagementBlockFactoryResetOnMobile": true,
  "deviceManagementBlockManualUnenroll": true,
  "safeSearchFilter": "strict",
  "edgeBlockPopups": true,
  "edgeBlockSearchSuggestions": true,
  "edgeBlockSendingIntranetTrafficToInternetExplorer": true,
  "edgeRequireSmartScreen": true,
  "edgeEnterpriseModeSiteListLocation": "Edge Enterprise Mode Site List Location value",
  "edgeFirstRunUrl": "https://example.com/edgeFirstRunUrl/",
  "edgeSearchEngine": {
    "@odata.type": "microsoft.graph.edgeSearchEngineBase"
  },
  "edgeHomepageUrls": [
    "Edge Homepage Urls value"
  ],
  "edgeBlockAccessToAboutFlags": true,
  "smartScreenBlockPromptOverride": true,
  "smartScreenBlockPromptOverrideForFiles": true,
  "webRtcBlockLocalhostIpAddress": true,
  "internetSharingBlocked": true,
  "settingsBlockAddProvisioningPackage": true,
  "settingsBlockRemoveProvisioningPackage": true,
  "settingsBlockChangeSystemTime": true,
  "settingsBlockEditDeviceName": true,
  "settingsBlockChangeRegion": true,
  "settingsBlockChangeLanguage": true,
  "settingsBlockChangePowerSleep": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "microsoftAccountBlockSettingsSync": true,
  "nfcBlocked": true,
  "resetProtectionModeBlocked": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireMobileDeviceEncryption": true,
  "usbBlocked": true,
  "voiceRecordingBlocked": true,
  "wiFiBlockAutomaticConnectHotspots": true,
  "wiFiBlocked": true,
  "wiFiBlockManualConfiguration": true,
  "wiFiScanInterval": 0,
  "wirelessDisplayBlockProjectionToThisDevice": true,
  "wirelessDisplayBlockUserInputFromReceiver": true,
  "wirelessDisplayRequirePinForPairing": true,
  "windowsStoreBlocked": true,
  "appsAllowTrustedAppsSideloading": "blocked",
  "windowsStoreBlockAutoUpdate": true,
  "developerUnlockSetting": "blocked",
  "sharedUserAppDataAllowed": true,
  "appsBlockWindowsStoreOriginatedApps": true,
  "windowsStoreEnablePrivateStoreOnly": true,
  "storageRestrictAppDataToSystemVolume": true,
  "storageRestrictAppInstallToSystemVolume": true,
  "gameDvrBlocked": true,
  "experienceBlockDeviceDiscovery": true,
  "experienceBlockErrorDialogWhenNoSIM": true,
  "experienceBlockTaskSwitcher": true,
  "logonBlockFastUserSwitching": true
}
```

### <a name="response"></a><span data-ttu-id="b8af8-812">応答</span><span class="sxs-lookup"><span data-stu-id="b8af8-812">Response</span></span>
<span data-ttu-id="b8af8-p156">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="b8af8-p156">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 9875

{
  "@odata.type": "#microsoft.graph.windows10GeneralConfiguration",
  "id": "a4235d71-5d71-a423-715d-23a4715d23a4",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "enterpriseCloudPrintDiscoveryEndPoint": "Enterprise Cloud Print Discovery End Point value",
  "enterpriseCloudPrintOAuthAuthority": "Enterprise Cloud Print OAuth Authority value",
  "enterpriseCloudPrintOAuthClientIdentifier": "Enterprise Cloud Print OAuth Client Identifier value",
  "enterpriseCloudPrintResourceIdentifier": "Enterprise Cloud Print Resource Identifier value",
  "enterpriseCloudPrintDiscoveryMaxLimit": 5,
  "enterpriseCloudPrintMopriaDiscoveryResourceIdentifier": "Enterprise Cloud Print Mopria Discovery Resource Identifier value",
  "searchBlockDiacritics": true,
  "searchDisableAutoLanguageDetection": true,
  "searchDisableIndexingEncryptedItems": true,
  "searchEnableRemoteQueries": true,
  "searchDisableIndexerBackoff": true,
  "searchDisableIndexingRemovableDrive": true,
  "searchEnableAutomaticIndexSizeManangement": true,
  "diagnosticsDataSubmissionMode": "none",
  "oneDriveDisableFileSync": true,
  "smartScreenEnableAppInstallControl": true,
  "personalizationDesktopImageUrl": "https://example.com/personalizationDesktopImageUrl/",
  "personalizationLockScreenImageUrl": "https://example.com/personalizationLockScreenImageUrl/",
  "bluetoothAllowedServices": [
    "Bluetooth Allowed Services value"
  ],
  "bluetoothBlockAdvertising": true,
  "bluetoothBlockDiscoverableMode": true,
  "bluetoothBlockPrePairing": true,
  "edgeBlockAutofill": true,
  "edgeBlocked": true,
  "edgeCookiePolicy": "allow",
  "edgeBlockDeveloperTools": true,
  "edgeBlockSendingDoNotTrackHeader": true,
  "edgeBlockExtensions": true,
  "edgeBlockInPrivateBrowsing": true,
  "edgeBlockJavaScript": true,
  "edgeBlockPasswordManager": true,
  "edgeBlockAddressBarDropdown": true,
  "edgeBlockCompatibilityList": true,
  "edgeClearBrowsingDataOnExit": true,
  "edgeAllowStartPagesModification": true,
  "edgeDisableFirstRunPage": true,
  "edgeBlockLiveTileDataCollection": true,
  "edgeSyncFavoritesWithInternetExplorer": true,
  "cellularBlockDataWhenRoaming": true,
  "cellularBlockVpn": true,
  "cellularBlockVpnWhenRoaming": true,
  "defenderBlockEndUserAccess": true,
  "defenderDaysBeforeDeletingQuarantinedMalware": 12,
  "defenderDetectedMalwareActions": {
    "@odata.type": "microsoft.graph.defenderDetectedMalwareActions",
    "lowSeverity": "clean",
    "moderateSeverity": "clean",
    "highSeverity": "clean",
    "severeSeverity": "clean"
  },
  "defenderSystemScanSchedule": "everyday",
  "defenderFilesAndFoldersToExclude": [
    "Defender Files And Folders To Exclude value"
  ],
  "defenderFileExtensionsToExclude": [
    "Defender File Extensions To Exclude value"
  ],
  "defenderScanMaxCpu": 2,
  "defenderMonitorFileActivity": "disable",
  "defenderProcessesToExclude": [
    "Defender Processes To Exclude value"
  ],
  "defenderPromptForSampleSubmission": "alwaysPrompt",
  "defenderRequireBehaviorMonitoring": true,
  "defenderRequireCloudProtection": true,
  "defenderRequireNetworkInspectionSystem": true,
  "defenderRequireRealTimeMonitoring": true,
  "defenderScanArchiveFiles": true,
  "defenderScanDownloads": true,
  "defenderScanNetworkFiles": true,
  "defenderScanIncomingMail": true,
  "defenderScanMappedNetworkDrivesDuringFullScan": true,
  "defenderScanRemovableDrivesDuringFullScan": true,
  "defenderScanScriptsLoadedInInternetExplorer": true,
  "defenderSignatureUpdateIntervalInHours": 6,
  "defenderScanType": "disabled",
  "defenderScheduledScanTime": "11:59:10.9990000",
  "defenderScheduledQuickScanTime": "11:58:49.3840000",
  "defenderCloudBlockLevel": "high",
  "lockScreenAllowTimeoutConfiguration": true,
  "lockScreenBlockActionCenterNotifications": true,
  "lockScreenBlockCortana": true,
  "lockScreenBlockToastNotifications": true,
  "lockScreenTimeoutInSeconds": 10,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordMinimumCharacterSetCount": 0,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordRequired": true,
  "passwordRequireWhenResumeFromIdleState": true,
  "passwordRequiredType": "alphanumeric",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "privacyAdvertisingId": "blocked",
  "privacyAutoAcceptPairingAndConsentPrompts": true,
  "privacyBlockInputPersonalization": true,
  "startBlockUnpinningAppsFromTaskbar": true,
  "startMenuAppListVisibility": "collapse",
  "startMenuHideChangeAccountSettings": true,
  "startMenuHideFrequentlyUsedApps": true,
  "startMenuHideHibernate": true,
  "startMenuHideLock": true,
  "startMenuHidePowerButton": true,
  "startMenuHideRecentJumpLists": true,
  "startMenuHideRecentlyAddedApps": true,
  "startMenuHideRestartOptions": true,
  "startMenuHideShutDown": true,
  "startMenuHideSignOut": true,
  "startMenuHideSleep": true,
  "startMenuHideSwitchAccount": true,
  "startMenuHideUserTile": true,
  "startMenuLayoutEdgeAssetsXml": "c3RhcnRNZW51TGF5b3V0RWRnZUFzc2V0c1htbA==",
  "startMenuLayoutXml": "c3RhcnRNZW51TGF5b3V0WG1s",
  "startMenuMode": "fullScreen",
  "startMenuPinnedFolderDocuments": "hide",
  "startMenuPinnedFolderDownloads": "hide",
  "startMenuPinnedFolderFileExplorer": "hide",
  "startMenuPinnedFolderHomeGroup": "hide",
  "startMenuPinnedFolderMusic": "hide",
  "startMenuPinnedFolderNetwork": "hide",
  "startMenuPinnedFolderPersonalFolder": "hide",
  "startMenuPinnedFolderPictures": "hide",
  "startMenuPinnedFolderSettings": "hide",
  "startMenuPinnedFolderVideos": "hide",
  "settingsBlockSettingsApp": true,
  "settingsBlockSystemPage": true,
  "settingsBlockDevicesPage": true,
  "settingsBlockNetworkInternetPage": true,
  "settingsBlockPersonalizationPage": true,
  "settingsBlockAccountsPage": true,
  "settingsBlockTimeLanguagePage": true,
  "settingsBlockEaseOfAccessPage": true,
  "settingsBlockPrivacyPage": true,
  "settingsBlockUpdateSecurityPage": true,
  "settingsBlockAppsPage": true,
  "settingsBlockGamingPage": true,
  "windowsSpotlightBlockConsumerSpecificFeatures": true,
  "windowsSpotlightBlocked": true,
  "windowsSpotlightBlockOnActionCenter": true,
  "windowsSpotlightBlockTailoredExperiences": true,
  "windowsSpotlightBlockThirdPartyNotifications": true,
  "windowsSpotlightBlockWelcomeExperience": true,
  "windowsSpotlightBlockWindowsTips": true,
  "windowsSpotlightConfigureOnLockScreen": "disabled",
  "networkProxyApplySettingsDeviceWide": true,
  "networkProxyDisableAutoDetect": true,
  "networkProxyAutomaticConfigurationUrl": "https://example.com/networkProxyAutomaticConfigurationUrl/",
  "networkProxyServer": {
    "@odata.type": "microsoft.graph.windows10NetworkProxyServer",
    "address": "Address value",
    "exceptions": [
      "Exceptions value"
    ],
    "useForLocalAddresses": true
  },
  "accountsBlockAddingNonMicrosoftAccountEmail": true,
  "antiTheftModeBlocked": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "connectedDevicesServiceBlocked": true,
  "certificatesBlockManualRootCertificateInstallation": true,
  "copyPasteBlocked": true,
  "cortanaBlocked": true,
  "deviceManagementBlockFactoryResetOnMobile": true,
  "deviceManagementBlockManualUnenroll": true,
  "safeSearchFilter": "strict",
  "edgeBlockPopups": true,
  "edgeBlockSearchSuggestions": true,
  "edgeBlockSendingIntranetTrafficToInternetExplorer": true,
  "edgeRequireSmartScreen": true,
  "edgeEnterpriseModeSiteListLocation": "Edge Enterprise Mode Site List Location value",
  "edgeFirstRunUrl": "https://example.com/edgeFirstRunUrl/",
  "edgeSearchEngine": {
    "@odata.type": "microsoft.graph.edgeSearchEngineBase"
  },
  "edgeHomepageUrls": [
    "Edge Homepage Urls value"
  ],
  "edgeBlockAccessToAboutFlags": true,
  "smartScreenBlockPromptOverride": true,
  "smartScreenBlockPromptOverrideForFiles": true,
  "webRtcBlockLocalhostIpAddress": true,
  "internetSharingBlocked": true,
  "settingsBlockAddProvisioningPackage": true,
  "settingsBlockRemoveProvisioningPackage": true,
  "settingsBlockChangeSystemTime": true,
  "settingsBlockEditDeviceName": true,
  "settingsBlockChangeRegion": true,
  "settingsBlockChangeLanguage": true,
  "settingsBlockChangePowerSleep": true,
  "locationServicesBlocked": true,
  "microsoftAccountBlocked": true,
  "microsoftAccountBlockSettingsSync": true,
  "nfcBlocked": true,
  "resetProtectionModeBlocked": true,
  "screenCaptureBlocked": true,
  "storageBlockRemovableStorage": true,
  "storageRequireMobileDeviceEncryption": true,
  "usbBlocked": true,
  "voiceRecordingBlocked": true,
  "wiFiBlockAutomaticConnectHotspots": true,
  "wiFiBlocked": true,
  "wiFiBlockManualConfiguration": true,
  "wiFiScanInterval": 0,
  "wirelessDisplayBlockProjectionToThisDevice": true,
  "wirelessDisplayBlockUserInputFromReceiver": true,
  "wirelessDisplayRequirePinForPairing": true,
  "windowsStoreBlocked": true,
  "appsAllowTrustedAppsSideloading": "blocked",
  "windowsStoreBlockAutoUpdate": true,
  "developerUnlockSetting": "blocked",
  "sharedUserAppDataAllowed": true,
  "appsBlockWindowsStoreOriginatedApps": true,
  "windowsStoreEnablePrivateStoreOnly": true,
  "storageRestrictAppDataToSystemVolume": true,
  "storageRestrictAppInstallToSystemVolume": true,
  "gameDvrBlocked": true,
  "experienceBlockDeviceDiscovery": true,
  "experienceBlockErrorDialogWhenNoSIM": true,
  "experienceBlockTaskSwitcher": true,
  "logonBlockFastUserSwitching": true
}
```


