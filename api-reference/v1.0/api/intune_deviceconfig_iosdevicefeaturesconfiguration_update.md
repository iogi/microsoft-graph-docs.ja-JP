# <a name="update-iosdevicefeaturesconfiguration"></a><span data-ttu-id="53640-101">Update iosDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="53640-101">Update iosDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="53640-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="53640-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53640-103">[iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="53640-103">Update the properties of a [calendar](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="53640-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="53640-104">Prerequisites</span></span>
<span data-ttu-id="53640-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53640-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="53640-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="53640-107">Permission type</span></span>|<span data-ttu-id="53640-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="53640-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="53640-109">委任 (職場または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="53640-109">Delegated (work or school account)</span></span>|<span data-ttu-id="53640-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="53640-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="53640-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="53640-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="53640-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="53640-112">Not supported.</span></span>|
|<span data-ttu-id="53640-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="53640-113">Application</span></span>|<span data-ttu-id="53640-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="53640-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="53640-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="53640-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="53640-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="53640-116">Request headers</span></span>
|<span data-ttu-id="53640-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="53640-117">Header</span></span>|<span data-ttu-id="53640-118">値</span><span class="sxs-lookup"><span data-stu-id="53640-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="53640-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="53640-119">Authorization</span></span>|<span data-ttu-id="53640-120">ベアラー &lt;トークン&gt; が必須。</span><span class="sxs-lookup"><span data-stu-id="53640-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="53640-121">Accept</span><span class="sxs-lookup"><span data-stu-id="53640-121">Accept</span></span>|<span data-ttu-id="53640-122">application/json</span><span class="sxs-lookup"><span data-stu-id="53640-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="53640-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="53640-123">Request body</span></span>
<span data-ttu-id="53640-124">要求本文で、[iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="53640-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) object.</span></span>

<span data-ttu-id="53640-125">次の表に、[iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="53640-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="53640-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="53640-126">Property</span></span>|<span data-ttu-id="53640-127">型</span><span class="sxs-lookup"><span data-stu-id="53640-127">Type</span></span>|<span data-ttu-id="53640-128">説明</span><span class="sxs-lookup"><span data-stu-id="53640-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53640-129">id</span><span class="sxs-lookup"><span data-stu-id="53640-129">id</span></span>|<span data-ttu-id="53640-130">String</span><span class="sxs-lookup"><span data-stu-id="53640-130">String</span></span>|<span data-ttu-id="53640-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="53640-131">Name of the entity.</span></span> <span data-ttu-id="53640-132">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="53640-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53640-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="53640-133">lastModifiedDateTime</span></span>|<span data-ttu-id="53640-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53640-134">DateTimeOffset</span></span>|<span data-ttu-id="53640-135">オブジェクトが最後に変更された DateTime。</span><span class="sxs-lookup"><span data-stu-id="53640-135">Gets or sets a DateTime value specifying when the node object was last modified.</span></span> <span data-ttu-id="53640-136">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="53640-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53640-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="53640-137">createdDateTime</span></span>|<span data-ttu-id="53640-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53640-138">DateTimeOffset</span></span>|<span data-ttu-id="53640-139">オブジェクトが作成された DateTime。</span><span class="sxs-lookup"><span data-stu-id="53640-139">DateTime the object was created.</span></span> <span data-ttu-id="53640-140">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="53640-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53640-141">description</span><span class="sxs-lookup"><span data-stu-id="53640-141">description</span></span>|<span data-ttu-id="53640-142">String</span><span class="sxs-lookup"><span data-stu-id="53640-142">String</span></span>|<span data-ttu-id="53640-143">デバイス構成について管理者が提供した説明。</span><span class="sxs-lookup"><span data-stu-id="53640-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="53640-144">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="53640-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53640-145">displayName</span><span class="sxs-lookup"><span data-stu-id="53640-145">displayName</span></span>|<span data-ttu-id="53640-146">String</span><span class="sxs-lookup"><span data-stu-id="53640-146">String</span></span>|<span data-ttu-id="53640-147">デバイス構成について管理者が指定した名前。</span><span class="sxs-lookup"><span data-stu-id="53640-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="53640-148">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="53640-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53640-149">version</span><span class="sxs-lookup"><span data-stu-id="53640-149">version</span></span>|<span data-ttu-id="53640-150">Int32</span><span class="sxs-lookup"><span data-stu-id="53640-150">Int32</span></span>|<span data-ttu-id="53640-151">デバイス構成のバージョン。</span><span class="sxs-lookup"><span data-stu-id="53640-151">Version of the device configuration.</span></span> <span data-ttu-id="53640-152">[deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="53640-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="53640-153">assetTagTemplate</span><span class="sxs-lookup"><span data-stu-id="53640-153">assetTagTemplate</span></span>|<span data-ttu-id="53640-154">String</span><span class="sxs-lookup"><span data-stu-id="53640-154">String</span></span>|<span data-ttu-id="53640-155">ログイン ウィンドウとロック画面に表示される、デバイスの資産タグ情報です。</span><span class="sxs-lookup"><span data-stu-id="53640-155">Asset tag information for the device, displayed on the login window and lock screen.</span></span>|
|<span data-ttu-id="53640-156">lockScreenFootnote</span><span class="sxs-lookup"><span data-stu-id="53640-156">lockScreenFootnote</span></span>|<span data-ttu-id="53640-157">String</span><span class="sxs-lookup"><span data-stu-id="53640-157">String</span></span>|<span data-ttu-id="53640-158">ログイン ウィンドウとロック画面に表示される脚注です。</span><span class="sxs-lookup"><span data-stu-id="53640-158">A footnote displayed on the login window and lock screen.</span></span> <span data-ttu-id="53640-159">IOS 9.3.1 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="53640-159">Available in iOS 9.3.1 and later.</span></span>|
|<span data-ttu-id="53640-160">homeScreenDockIcons</span><span class="sxs-lookup"><span data-stu-id="53640-160">homeScreenDockIcons</span></span>|<span data-ttu-id="53640-161">[iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="53640-161">[iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="53640-162">ホーム画面ドックに表示されるアプリとフォルダーのリスト。</span><span class="sxs-lookup"><span data-stu-id="53640-162">A list of app and folders to appear on the Home Screen Dock.</span></span> <span data-ttu-id="53640-163">このコレクションには、最大で 500 個の要素を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="53640-163">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="53640-164">homeScreenPages</span><span class="sxs-lookup"><span data-stu-id="53640-164">homeScreenPages</span></span>|<span data-ttu-id="53640-165">[iosHomeScreenPage](../resources/intune_deviceconfig_ioshomescreenpage.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="53640-165">[iosHomeScreenPage](../resources/intune_deviceconfig_ioshomescreenpage.md) collection</span></span>|<span data-ttu-id="53640-166">ホーム画面上のページのリスト。</span><span class="sxs-lookup"><span data-stu-id="53640-166">A list of pages on the Home Screen.</span></span> <span data-ttu-id="53640-167">このコレクションには、最大で 500 個の要素を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="53640-167">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="53640-168">notificationSettings</span><span class="sxs-lookup"><span data-stu-id="53640-168">notificationSettings</span></span>|<span data-ttu-id="53640-169">[iosNotificationSettings](../resources/intune_deviceconfig_iosnotificationsettings.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="53640-169">[iosNotificationSettings](../resources/intune_deviceconfig_iosnotificationsettings.md) collection</span></span>|<span data-ttu-id="53640-170">各バンドル ID ごとの通知設定。監視モードのデバイスにのみ (iOS 9.3 以降) 適用されます。</span><span class="sxs-lookup"><span data-stu-id="53640-170">Notification settings for each bundle id. Applicable to devices in supervised mode only (iOS 9.3 and later).</span></span> <span data-ttu-id="53640-171">このコレクションには、最大で 500 個の要素を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="53640-171">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="53640-172">応答</span><span class="sxs-lookup"><span data-stu-id="53640-172">Response</span></span>
<span data-ttu-id="53640-173">このメソッドが成功した場合、このメソッドは `200 OK` 応答コードと、更新された [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) オブジェクトを応答本文で返します。</span><span class="sxs-lookup"><span data-stu-id="53640-173">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="53640-174">例</span><span class="sxs-lookup"><span data-stu-id="53640-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="53640-175">要求</span><span class="sxs-lookup"><span data-stu-id="53640-175">Request</span></span>
<span data-ttu-id="53640-176">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="53640-176">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1983

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="53640-177">応答</span><span class="sxs-lookup"><span data-stu-id="53640-177">Response</span></span>
<span data-ttu-id="53640-p112">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="53640-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2160

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```


