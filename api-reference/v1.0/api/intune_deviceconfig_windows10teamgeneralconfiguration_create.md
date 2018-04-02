# <a name="create-windows10teamgeneralconfiguration"></a><span data-ttu-id="46ddd-101">windows10TeamGeneralConfiguration の作成</span><span class="sxs-lookup"><span data-stu-id="46ddd-101">Create windows10TeamGeneralConfiguration</span></span>

> <span data-ttu-id="46ddd-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="46ddd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="46ddd-103">新しい [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-103">Create a new [plannerBucket](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="46ddd-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="46ddd-104">Prerequisites</span></span>
<span data-ttu-id="46ddd-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="46ddd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="46ddd-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="46ddd-107">Permission type</span></span>|<span data-ttu-id="46ddd-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="46ddd-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="46ddd-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="46ddd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="46ddd-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="46ddd-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="46ddd-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="46ddd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="46ddd-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="46ddd-112">Not supported.</span></span>|
|<span data-ttu-id="46ddd-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="46ddd-113">Application</span></span>|<span data-ttu-id="46ddd-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="46ddd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="46ddd-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="46ddd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="46ddd-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="46ddd-116">Request headers</span></span>
|<span data-ttu-id="46ddd-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="46ddd-117">Header</span></span>|<span data-ttu-id="46ddd-118">値</span><span class="sxs-lookup"><span data-stu-id="46ddd-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="46ddd-119">承認</span><span class="sxs-lookup"><span data-stu-id="46ddd-119">Authorization</span></span>|<span data-ttu-id="46ddd-120">ベアラー &lt;トークン&gt;が必須。</span><span class="sxs-lookup"><span data-stu-id="46ddd-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="46ddd-121">承諾</span><span class="sxs-lookup"><span data-stu-id="46ddd-121">Accept</span></span>|<span data-ttu-id="46ddd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="46ddd-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="46ddd-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="46ddd-123">Request body</span></span>
<span data-ttu-id="46ddd-124">要求本文で、windows10TeamGeneralConfiguration オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="46ddd-125">次の表に、windows10TeamGeneralConfiguration の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="46ddd-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="46ddd-126">Property</span></span>|<span data-ttu-id="46ddd-127">型</span><span class="sxs-lookup"><span data-stu-id="46ddd-127">Type</span></span>|<span data-ttu-id="46ddd-128">説明</span><span class="sxs-lookup"><span data-stu-id="46ddd-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="46ddd-129">id</span><span class="sxs-lookup"><span data-stu-id="46ddd-129">id</span></span>|<span data-ttu-id="46ddd-130">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-130">String</span></span>|<span data-ttu-id="46ddd-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="46ddd-131">Name of the entity.</span></span> <span data-ttu-id="46ddd-132">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="46ddd-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46ddd-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="46ddd-133">lastModifiedDateTime</span></span>|<span data-ttu-id="46ddd-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46ddd-134">DateTimeOffset</span></span>|<span data-ttu-id="46ddd-135">オブジェクトの最終更新の DateTime。</span><span class="sxs-lookup"><span data-stu-id="46ddd-135">Gets or sets a DateTime value specifying when the node object was last modified.</span></span> <span data-ttu-id="46ddd-136">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="46ddd-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46ddd-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="46ddd-137">createdDateTime</span></span>|<span data-ttu-id="46ddd-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="46ddd-138">DateTimeOffset</span></span>|<span data-ttu-id="46ddd-139">オブジェクトが作成された DateTime。</span><span class="sxs-lookup"><span data-stu-id="46ddd-139">DateTime the object was created.</span></span> <span data-ttu-id="46ddd-140">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="46ddd-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46ddd-141">description</span><span class="sxs-lookup"><span data-stu-id="46ddd-141">description</span></span>|<span data-ttu-id="46ddd-142">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-142">String</span></span>|<span data-ttu-id="46ddd-143">デバイス構成について管理者が提供した説明。</span><span class="sxs-lookup"><span data-stu-id="46ddd-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="46ddd-144">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="46ddd-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46ddd-145">displayName</span><span class="sxs-lookup"><span data-stu-id="46ddd-145">displayName</span></span>|<span data-ttu-id="46ddd-146">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-146">String</span></span>|<span data-ttu-id="46ddd-147">デバイス構成について管理者が指定した名前。</span><span class="sxs-lookup"><span data-stu-id="46ddd-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="46ddd-148">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="46ddd-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46ddd-149">version</span><span class="sxs-lookup"><span data-stu-id="46ddd-149">version</span></span>|<span data-ttu-id="46ddd-150">Int32</span><span class="sxs-lookup"><span data-stu-id="46ddd-150">Int32</span></span>|<span data-ttu-id="46ddd-151">デバイス構成のバージョン。</span><span class="sxs-lookup"><span data-stu-id="46ddd-151">Version of the device configuration.</span></span> <span data-ttu-id="46ddd-152">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="46ddd-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="46ddd-153">azureOperationalInsightsBlockTelemetry</span><span class="sxs-lookup"><span data-stu-id="46ddd-153">azureOperationalInsightsBlockTelemetry</span></span>|<span data-ttu-id="46ddd-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-154">Boolean</span></span>|<span data-ttu-id="46ddd-155">Azure Operational Insights をブロックするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-155">Indicates whether or not to Block Azure Operational Insights.</span></span>|
|<span data-ttu-id="46ddd-156">azureOperationalInsightsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="46ddd-156">azureOperationalInsightsWorkspaceId</span></span>|<span data-ttu-id="46ddd-157">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-157">String</span></span>|<span data-ttu-id="46ddd-158">Azure Operational Insights のワークスペース ID。</span><span class="sxs-lookup"><span data-stu-id="46ddd-158">The Azure Operational Insights workspace id.</span></span>|
|<span data-ttu-id="46ddd-159">azureOperationalInsightsWorkspaceKey</span><span class="sxs-lookup"><span data-stu-id="46ddd-159">azureOperationalInsightsWorkspaceKey</span></span>|<span data-ttu-id="46ddd-160">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-160">String</span></span>|<span data-ttu-id="46ddd-161">Azure Operational Insights のワークスペース キー。</span><span class="sxs-lookup"><span data-stu-id="46ddd-161">The Azure Operational Insights Workspace key.</span></span>|
|<span data-ttu-id="46ddd-162">connectAppBlockAutoLaunch</span><span class="sxs-lookup"><span data-stu-id="46ddd-162">connectAppBlockAutoLaunch</span></span>|<span data-ttu-id="46ddd-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-163">Boolean</span></span>|<span data-ttu-id="46ddd-164">投影を開始するたびに、接続アプリを自動的に起動するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-164">Specifies whether to automatically launch the Connect app whenever a projection is initiated.</span></span>|
|<span data-ttu-id="46ddd-165">maintenanceWindowBlocked</span><span class="sxs-lookup"><span data-stu-id="46ddd-165">maintenanceWindowBlocked</span></span>|<span data-ttu-id="46ddd-166">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-166">Boolean</span></span>|<span data-ttu-id="46ddd-167">デバイス更新のメンテナンス ウィンドウの設定をブロックするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-167">Indicates whether or not to Block setting a maintenance window for device updates.</span></span>|
|<span data-ttu-id="46ddd-168">maintenanceWindowDurationInHours</span><span class="sxs-lookup"><span data-stu-id="46ddd-168">maintenanceWindowDurationInHours</span></span>|<span data-ttu-id="46ddd-169">Int32</span><span class="sxs-lookup"><span data-stu-id="46ddd-169">Int32</span></span>|<span data-ttu-id="46ddd-170">デバイス更新のためのメンテナンス期間の長さ (時間)。</span><span class="sxs-lookup"><span data-stu-id="46ddd-170">Maintenance window duration for device updates.</span></span> <span data-ttu-id="46ddd-171">有効な値は 1 から 5 までです</span><span class="sxs-lookup"><span data-stu-id="46ddd-171">Valid values 1 to 5</span></span>|
|<span data-ttu-id="46ddd-172">maintenanceWindowStartTime</span><span class="sxs-lookup"><span data-stu-id="46ddd-172">maintenanceWindowStartTime</span></span>|<span data-ttu-id="46ddd-173">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="46ddd-173">TimeOfDay</span></span>|<span data-ttu-id="46ddd-174">デバイス更新のためのメンテナンス期間の開始時刻。</span><span class="sxs-lookup"><span data-stu-id="46ddd-174">Maintenance window start time for device updates.</span></span>|
|<span data-ttu-id="46ddd-175">miracastChannel</span><span class="sxs-lookup"><span data-stu-id="46ddd-175">miracastChannel</span></span>|<span data-ttu-id="46ddd-176">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-176">String</span></span>|<span data-ttu-id="46ddd-177">チャネル。</span><span class="sxs-lookup"><span data-stu-id="46ddd-177">The channel.</span></span> <span data-ttu-id="46ddd-178">可能な値は、`userDefined`、`one`、`two`、`three`、`four`、`five`、`six`、`seven`、`eight`、`nine`、`ten`、`eleven`、`thirtySix`、`forty`、`fortyFour`、`fortyEight`、`oneHundredFortyNine`、`oneHundredFiftyThree`、`oneHundredFiftySeven`、`oneHundredSixtyOne`、`oneHundredSixtyFive` です。</span><span class="sxs-lookup"><span data-stu-id="46ddd-178">Possible values are: `userDefined`, `one`, `two`, `three`, `four`, `five`, `six`, `seven`, `eight`, `nine`, `ten`, `eleven`, `thirtySix`, `forty`, `fortyFour`, `fortyEight`, `oneHundredFortyNine`, `oneHundredFiftyThree`, `oneHundredFiftySeven`, `oneHundredSixtyOne`, `oneHundredSixtyFive`.</span></span>|
|<span data-ttu-id="46ddd-179">miracastBlocked</span><span class="sxs-lookup"><span data-stu-id="46ddd-179">miracastBlocked</span></span>|<span data-ttu-id="46ddd-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-180">Boolean</span></span>|<span data-ttu-id="46ddd-181">ワイヤレス投影をブロックするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-181">Indicates whether or not to Block wireless projection.</span></span>|
|<span data-ttu-id="46ddd-182">miracastRequirePin</span><span class="sxs-lookup"><span data-stu-id="46ddd-182">miracastRequirePin</span></span>|<span data-ttu-id="46ddd-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-183">Boolean</span></span>|<span data-ttu-id="46ddd-184">ワイヤレス投影の pin が必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-184">Indicates whether or not to require a pin for wireless projection.</span></span>|
|<span data-ttu-id="46ddd-185">settingsBlockMyMeetingsAndFiles</span><span class="sxs-lookup"><span data-stu-id="46ddd-185">settingsBlockMyMeetingsAndFiles</span></span>|<span data-ttu-id="46ddd-186">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-186">Boolean</span></span>|<span data-ttu-id="46ddd-187">スタート メニューで [会議とファイル] 機能を無効にするかどうかを指定します。この機能は、サインイン ユーザーの会議とファイルを Office 365 から表示します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-187">Specifies whether to disable the "My meetings and files" feature in the Start menu, which shows the signed-in user's meetings and files from Office 365.</span></span>|
|<span data-ttu-id="46ddd-188">settingsBlockSessionResume</span><span class="sxs-lookup"><span data-stu-id="46ddd-188">settingsBlockSessionResume</span></span>|<span data-ttu-id="46ddd-189">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-189">Boolean</span></span>|<span data-ttu-id="46ddd-190">セッションがタイムアウトになった際にセッションを再開する機能を許可するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-190">Specifies whether to allow the ability to resume a session when the session times out.</span></span>|
|<span data-ttu-id="46ddd-191">settingsBlockSigninSuggestions</span><span class="sxs-lookup"><span data-stu-id="46ddd-191">settingsBlockSigninSuggestions</span></span>|<span data-ttu-id="46ddd-192">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-192">Boolean</span></span>|<span data-ttu-id="46ddd-193">スケジュールされている会議の招待者をサインイン ダイアログに自動入力する機能を無効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-193">Specifies whether to disable auto-populating of the sign-in dialog with invitees from scheduled meetings.</span></span>|
|<span data-ttu-id="46ddd-194">settingsDefaultVolume</span><span class="sxs-lookup"><span data-stu-id="46ddd-194">settingsDefaultVolume</span></span>|<span data-ttu-id="46ddd-195">Int32</span><span class="sxs-lookup"><span data-stu-id="46ddd-195">Int32</span></span>|<span data-ttu-id="46ddd-196">新しいセッションの既定のボリューム値を指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-196">Specifies the default volume value for a new session.</span></span> <span data-ttu-id="46ddd-197">許可される値は、0 から 100 までです。</span><span class="sxs-lookup"><span data-stu-id="46ddd-197">Permitted values are 0-100.</span></span> <span data-ttu-id="46ddd-198">既定値は 45 です。</span><span class="sxs-lookup"><span data-stu-id="46ddd-198">The default is 45.</span></span> <span data-ttu-id="46ddd-199">有効な値は 0 から 100 までです</span><span class="sxs-lookup"><span data-stu-id="46ddd-199">Valid values 0 to 100</span></span>|
|<span data-ttu-id="46ddd-200">settingsScreenTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="46ddd-200">settingsScreenTimeoutInMinutes</span></span>|<span data-ttu-id="46ddd-201">Int32</span><span class="sxs-lookup"><span data-stu-id="46ddd-201">Int32</span></span>|<span data-ttu-id="46ddd-202">ハブ スクリーンがオフになるまでの分数を指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-202">Specifies the number of minutes until the Hub screen turns off.</span></span>|
|<span data-ttu-id="46ddd-203">settingsSessionTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="46ddd-203">settingsSessionTimeoutInMinutes</span></span>|<span data-ttu-id="46ddd-204">Int32</span><span class="sxs-lookup"><span data-stu-id="46ddd-204">Int32</span></span>|<span data-ttu-id="46ddd-205">セッションがタイムアウトになるまでの分数を指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-205">Specifies the number of minutes until the session times out.</span></span>|
|<span data-ttu-id="46ddd-206">settingsSleepTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="46ddd-206">settingsSleepTimeoutInMinutes</span></span>|<span data-ttu-id="46ddd-207">Int32</span><span class="sxs-lookup"><span data-stu-id="46ddd-207">Int32</span></span>|<span data-ttu-id="46ddd-208">ハブがスリープ モードになるまでの分数を指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-208">Specifies the number of minutes until the Hub enters sleep mode.</span></span>|
|<span data-ttu-id="46ddd-209">welcomeScreenBlockAutomaticWakeUp</span><span class="sxs-lookup"><span data-stu-id="46ddd-209">welcomeScreenBlockAutomaticWakeUp</span></span>|<span data-ttu-id="46ddd-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="46ddd-210">Boolean</span></span>|<span data-ttu-id="46ddd-211">ユーザーが入室した際に、ようこそ画面が自動的に起動するのをブロックするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-211">Indicates whether or not to Block the welcome screen from waking up automatically when someone enters the room.</span></span>|
|<span data-ttu-id="46ddd-212">welcomeScreenBackgroundImageUrl</span><span class="sxs-lookup"><span data-stu-id="46ddd-212">welcomeScreenBackgroundImageUrl</span></span>|<span data-ttu-id="46ddd-213">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-213">String</span></span>|<span data-ttu-id="46ddd-214">ようこそ画面の背景画像の URL。</span><span class="sxs-lookup"><span data-stu-id="46ddd-214">The welcome screen background image URL.</span></span> <span data-ttu-id="46ddd-215">URL は HTTPS プロトコルを使用し、PNG 画像を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="46ddd-215">The URL must use the HTTPS protocol and return a PNG image.</span></span>|
|<span data-ttu-id="46ddd-216">welcomeScreenMeetingInformation</span><span class="sxs-lookup"><span data-stu-id="46ddd-216">welcomeScreenMeetingInformation</span></span>|<span data-ttu-id="46ddd-217">String</span><span class="sxs-lookup"><span data-stu-id="46ddd-217">String</span></span>|<span data-ttu-id="46ddd-218">表示される、ようこそ画面の会議情報。</span><span class="sxs-lookup"><span data-stu-id="46ddd-218">The welcome screen meeting information shown.</span></span> <span data-ttu-id="46ddd-219">可能な値は、`userDefined`、`showOrganizerAndTimeOnly`、`showOrganizerAndTimeAndSubject` です。</span><span class="sxs-lookup"><span data-stu-id="46ddd-219">Possible values are: `userDefined`, `showOrganizerAndTimeOnly`, `showOrganizerAndTimeAndSubject`.</span></span>|



## <a name="response"></a><span data-ttu-id="46ddd-220">応答</span><span class="sxs-lookup"><span data-stu-id="46ddd-220">Response</span></span>
<span data-ttu-id="46ddd-221">このメソッドが成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [windows10TeamGeneralConfiguration](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="46ddd-221">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_windows10teamgeneralconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="46ddd-222">例</span><span class="sxs-lookup"><span data-stu-id="46ddd-222">Example</span></span>
### <a name="request"></a><span data-ttu-id="46ddd-223">要求</span><span class="sxs-lookup"><span data-stu-id="46ddd-223">Request</span></span>
<span data-ttu-id="46ddd-224">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="46ddd-224">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1214

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```

### <a name="response"></a><span data-ttu-id="46ddd-225">応答</span><span class="sxs-lookup"><span data-stu-id="46ddd-225">Response</span></span>
<span data-ttu-id="46ddd-p113">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="46ddd-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1322

{
  "@odata.type": "#microsoft.graph.windows10TeamGeneralConfiguration",
  "id": "0c94aa20-aa20-0c94-20aa-940c20aa940c",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "azureOperationalInsightsBlockTelemetry": true,
  "azureOperationalInsightsWorkspaceId": "Azure Operational Insights Workspace Id value",
  "azureOperationalInsightsWorkspaceKey": "Azure Operational Insights Workspace Key value",
  "connectAppBlockAutoLaunch": true,
  "maintenanceWindowBlocked": true,
  "maintenanceWindowDurationInHours": 0,
  "maintenanceWindowStartTime": "11:59:09.3130000",
  "miracastChannel": "one",
  "miracastBlocked": true,
  "miracastRequirePin": true,
  "settingsBlockMyMeetingsAndFiles": true,
  "settingsBlockSessionResume": true,
  "settingsBlockSigninSuggestions": true,
  "settingsDefaultVolume": 5,
  "settingsScreenTimeoutInMinutes": 14,
  "settingsSessionTimeoutInMinutes": 15,
  "settingsSleepTimeoutInMinutes": 13,
  "welcomeScreenBlockAutomaticWakeUp": true,
  "welcomeScreenBackgroundImageUrl": "https://example.com/welcomeScreenBackgroundImageUrl/",
  "welcomeScreenMeetingInformation": "showOrganizerAndTimeOnly"
}
```


