# <a name="update-macosofficesuiteapp"></a><span data-ttu-id="82de2-101">macOSOfficeSuiteApp の更新</span><span class="sxs-lookup"><span data-stu-id="82de2-101">Update macOSOfficeSuiteApp</span></span>

> <span data-ttu-id="82de2-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="82de2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82de2-103">[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトのプロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="82de2-103">Update the properties of a [calendar](../resources/intune_apps_macosofficesuiteapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="82de2-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="82de2-104">Prerequisites</span></span>
<span data-ttu-id="82de2-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82de2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="82de2-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="82de2-107">Permission type</span></span>|<span data-ttu-id="82de2-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="82de2-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="82de2-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="82de2-109">Delegated (work or school account)</span></span>|<span data-ttu-id="82de2-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="82de2-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="82de2-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="82de2-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="82de2-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="82de2-112">Not supported.</span></span>|
|<span data-ttu-id="82de2-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="82de2-113">Application</span></span>|<span data-ttu-id="82de2-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="82de2-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="82de2-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="82de2-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}
```

## <a name="request-headers"></a><span data-ttu-id="82de2-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="82de2-116">Request headers</span></span>
|<span data-ttu-id="82de2-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="82de2-117">Header</span></span>|<span data-ttu-id="82de2-118">値</span><span class="sxs-lookup"><span data-stu-id="82de2-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="82de2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="82de2-119">Authorization</span></span>|<span data-ttu-id="82de2-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="82de2-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="82de2-121">Accept</span><span class="sxs-lookup"><span data-stu-id="82de2-121">Accept</span></span>|<span data-ttu-id="82de2-122">application/json</span><span class="sxs-lookup"><span data-stu-id="82de2-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="82de2-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="82de2-123">Request body</span></span>
<span data-ttu-id="82de2-124">要求本文で、[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="82de2-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_apps_macosofficesuiteapp.md) object.</span></span>

<span data-ttu-id="82de2-125">次の表に、[macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="82de2-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="82de2-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="82de2-126">Property</span></span>|<span data-ttu-id="82de2-127">型</span><span class="sxs-lookup"><span data-stu-id="82de2-127">Type</span></span>|<span data-ttu-id="82de2-128">説明</span><span class="sxs-lookup"><span data-stu-id="82de2-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82de2-129">id</span><span class="sxs-lookup"><span data-stu-id="82de2-129">id</span></span>|<span data-ttu-id="82de2-130">String</span><span class="sxs-lookup"><span data-stu-id="82de2-130">String</span></span>|<span data-ttu-id="82de2-131">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="82de2-131">Name of the entity.</span></span> <span data-ttu-id="82de2-132">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-132">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-133">displayName</span><span class="sxs-lookup"><span data-stu-id="82de2-133">displayName</span></span>|<span data-ttu-id="82de2-134">String</span><span class="sxs-lookup"><span data-stu-id="82de2-134">String</span></span>|<span data-ttu-id="82de2-135">管理者が指定またはインポートした、アプリのタイトル。</span><span class="sxs-lookup"><span data-stu-id="82de2-135">The admin provided or imported title of the app.</span></span> <span data-ttu-id="82de2-136">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-136">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-137">description</span><span class="sxs-lookup"><span data-stu-id="82de2-137">description</span></span>|<span data-ttu-id="82de2-138">String</span><span class="sxs-lookup"><span data-stu-id="82de2-138">String</span></span>|<span data-ttu-id="82de2-139">アプリの説明。</span><span class="sxs-lookup"><span data-stu-id="82de2-139">The description of the app.</span></span> <span data-ttu-id="82de2-140">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-140">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-141">publisher</span><span class="sxs-lookup"><span data-stu-id="82de2-141">Publisher</span></span>|<span data-ttu-id="82de2-142">String</span><span class="sxs-lookup"><span data-stu-id="82de2-142">String</span></span>|<span data-ttu-id="82de2-143">アプリの発行元。</span><span class="sxs-lookup"><span data-stu-id="82de2-143">The name of the app.</span></span> <span data-ttu-id="82de2-144">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-144">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-145">largeIcon</span><span class="sxs-lookup"><span data-stu-id="82de2-145">largeIcon</span></span>|[<span data-ttu-id="82de2-146">mimeContent</span><span class="sxs-lookup"><span data-stu-id="82de2-146">MimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="82de2-147">アプリの詳細に表示され、アイコンのアップロードに使用される大きいアイコン。</span><span class="sxs-lookup"><span data-stu-id="82de2-147">The large icon, to be displayed in the app details and used for upload of the icon.</span></span> <span data-ttu-id="82de2-148">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-148">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-149">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="82de2-149">createdDateTime</span></span>|<span data-ttu-id="82de2-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="82de2-150">DateTimeOffset</span></span>|<span data-ttu-id="82de2-151">アプリが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="82de2-151">The date and time when the page was created.</span></span> <span data-ttu-id="82de2-152">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-152">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-153">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="82de2-153">lastModifiedDateTime</span></span>|<span data-ttu-id="82de2-154">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="82de2-154">DateTimeOffset</span></span>|<span data-ttu-id="82de2-155">アプリが最後に変更された日時。</span><span class="sxs-lookup"><span data-stu-id="82de2-155">The date and time when the attachment was last modified.</span></span> <span data-ttu-id="82de2-156">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-156">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-157">isFeatured</span><span class="sxs-lookup"><span data-stu-id="82de2-157">isFeatured</span></span>|<span data-ttu-id="82de2-158">Boolean</span><span class="sxs-lookup"><span data-stu-id="82de2-158">Boolean</span></span>|<span data-ttu-id="82de2-159">アプリが管理者のおすすめとしてマークされたかどうかを示す値。[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-159">The value indicating whether the app is marked as featured by the admin. Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-160">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="82de2-160">privacyInformationUrl</span></span>|<span data-ttu-id="82de2-161">String</span><span class="sxs-lookup"><span data-stu-id="82de2-161">String</span></span>|<span data-ttu-id="82de2-162">プライバシーに関する声明の URL。</span><span class="sxs-lookup"><span data-stu-id="82de2-162">The privacy statement Url.</span></span> <span data-ttu-id="82de2-163">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-163">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-164">informationUrl</span><span class="sxs-lookup"><span data-stu-id="82de2-164">informationUrl</span></span>|<span data-ttu-id="82de2-165">String</span><span class="sxs-lookup"><span data-stu-id="82de2-165">String</span></span>|<span data-ttu-id="82de2-166">詳細情報の URL。</span><span class="sxs-lookup"><span data-stu-id="82de2-166">The more information Url.</span></span> <span data-ttu-id="82de2-167">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-167">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-168">owner</span><span class="sxs-lookup"><span data-stu-id="82de2-168">owner</span></span>|<span data-ttu-id="82de2-169">String</span><span class="sxs-lookup"><span data-stu-id="82de2-169">String</span></span>|<span data-ttu-id="82de2-170">アプリの所有者。</span><span class="sxs-lookup"><span data-stu-id="82de2-170">The owner of the timesheet.</span></span> <span data-ttu-id="82de2-171">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-171">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-172">developer</span><span class="sxs-lookup"><span data-stu-id="82de2-172">developer</span></span>|<span data-ttu-id="82de2-173">String</span><span class="sxs-lookup"><span data-stu-id="82de2-173">String</span></span>|<span data-ttu-id="82de2-174">アプリの開発者。</span><span class="sxs-lookup"><span data-stu-id="82de2-174">The name of the app.</span></span> <span data-ttu-id="82de2-175">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-175">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-176">notes</span><span class="sxs-lookup"><span data-stu-id="82de2-176">notes</span></span>|<span data-ttu-id="82de2-177">String</span><span class="sxs-lookup"><span data-stu-id="82de2-177">String</span></span>|<span data-ttu-id="82de2-178">アプリ用のメモ。</span><span class="sxs-lookup"><span data-stu-id="82de2-178">Notes for the app.</span></span> <span data-ttu-id="82de2-179">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="82de2-179">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md)</span></span>|
|<span data-ttu-id="82de2-180">publishingState</span><span class="sxs-lookup"><span data-stu-id="82de2-180">publishingState</span></span>|<span data-ttu-id="82de2-181">String</span><span class="sxs-lookup"><span data-stu-id="82de2-181">String</span></span>|<span data-ttu-id="82de2-182">アプリの発行状態。</span><span class="sxs-lookup"><span data-stu-id="82de2-182">The publishing state for the app.</span></span> <span data-ttu-id="82de2-183">アプリが発行されていないと、アプリを割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="82de2-183">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="82de2-184">[mobileApp](../resources/intune_apps_mobileapp.md) から継承します。可能な値は、`notPublished`、`processing`、`published` です。</span><span class="sxs-lookup"><span data-stu-id="82de2-184">Inherited from [mobileApp](../resources/intune_apps_mobileapp.md) Possible values are: `notPublished`, `processing`, `published`.</span></span>|



## <a name="response"></a><span data-ttu-id="82de2-185">応答</span><span class="sxs-lookup"><span data-stu-id="82de2-185">Response</span></span>
<span data-ttu-id="82de2-186">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で更新された [macOSOfficeSuiteApp](../resources/intune_apps_macosofficesuiteapp.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="82de2-186">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_apps_macosofficesuiteapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="82de2-187">例</span><span class="sxs-lookup"><span data-stu-id="82de2-187">Example</span></span>
### <a name="request"></a><span data-ttu-id="82de2-188">要求</span><span class="sxs-lookup"><span data-stu-id="82de2-188">Request</span></span>
<span data-ttu-id="82de2-189">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="82de2-189">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileApps/{mobileAppId}
Content-type: application/json
Content-length: 590

{
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
  "publishingState": "processing"
}
```

### <a name="response"></a><span data-ttu-id="82de2-190">応答</span><span class="sxs-lookup"><span data-stu-id="82de2-190">Response</span></span>
<span data-ttu-id="82de2-p115">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="82de2-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 756

{
  "@odata.type": "#microsoft.graph.macOSOfficeSuiteApp",
  "id": "bf39e35d-e35d-bf39-5de3-39bf5de339bf",
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
  "publishingState": "processing"
}
```


