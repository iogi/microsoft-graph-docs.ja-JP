# <a name="mobileapp-resource-type"></a><span data-ttu-id="2c49c-101">mobileApp リソースの種類</span><span class="sxs-lookup"><span data-stu-id="2c49c-101">mobileApp resource type</span></span>

> <span data-ttu-id="2c49c-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c49c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2c49c-103">Intune モバイル アプリの基本プロパティを含む抽象クラスです。</span><span class="sxs-lookup"><span data-stu-id="2c49c-103">An abstract class containing the base properties for Intune mobile apps.</span></span>
## <a name="methods"></a><span data-ttu-id="2c49c-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="2c49c-104">Methods</span></span>
|<span data-ttu-id="2c49c-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="2c49c-105">Method</span></span>|<span data-ttu-id="2c49c-106">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="2c49c-106">Return Type</span></span>|<span data-ttu-id="2c49c-107">説明</span><span class="sxs-lookup"><span data-stu-id="2c49c-107">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="2c49c-108">mobileApps のリスト</span><span class="sxs-lookup"><span data-stu-id="2c49c-108">List mobileApps</span></span>](../api/intune_apps_mobileapp_list.md)|<span data-ttu-id="2c49c-109">[mobileApp](../resources/intune_apps_mobileapp.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="2c49c-109">[mobileApp](../resources/intune_apps_mobileapp.md) collection</span></span>|<span data-ttu-id="2c49c-110">[mobileApp](../resources/intune_apps_mobileapp.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="2c49c-110">List properties and relationships of the [mobileApp](../resources/intune_apps_mobileapp.md) objects.</span></span>|
|[<span data-ttu-id="2c49c-111">MobileApp の取得</span><span class="sxs-lookup"><span data-stu-id="2c49c-111">Get mobileApp</span></span>](../api/intune_apps_mobileapp_get.md)|[<span data-ttu-id="2c49c-112">mobileApp</span><span class="sxs-lookup"><span data-stu-id="2c49c-112">mobileApp</span></span>](../resources/intune_apps_mobileapp.md)|<span data-ttu-id="2c49c-113">[mobileApp](../resources/intune_apps_mobileapp.md) オブジェクトのプロパティとリレーションシップを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2c49c-113">Read properties and relationships of [plannerTaskDetails](../resources/intune_apps_mobileapp.md) object.</span></span>|
|[<span data-ttu-id="2c49c-114">アクションの割り当て</span><span class="sxs-lookup"><span data-stu-id="2c49c-114">assign action</span></span>](../api/intune_apps_mobileapp_assign.md)|<span data-ttu-id="2c49c-115">なし</span><span class="sxs-lookup"><span data-stu-id="2c49c-115">None</span></span>|<span data-ttu-id="2c49c-116">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="2c49c-116">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="2c49c-117">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c49c-117">Properties</span></span>
|<span data-ttu-id="2c49c-118">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c49c-118">Property</span></span>|<span data-ttu-id="2c49c-119">型</span><span class="sxs-lookup"><span data-stu-id="2c49c-119">Type</span></span>|<span data-ttu-id="2c49c-120">説明</span><span class="sxs-lookup"><span data-stu-id="2c49c-120">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2c49c-121">id</span><span class="sxs-lookup"><span data-stu-id="2c49c-121">id</span></span>|<span data-ttu-id="2c49c-122">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-122">String</span></span>|<span data-ttu-id="2c49c-123">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="2c49c-123">Name of the entity.</span></span>|
|<span data-ttu-id="2c49c-124">displayName</span><span class="sxs-lookup"><span data-stu-id="2c49c-124">displayName</span></span>|<span data-ttu-id="2c49c-125">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-125">String</span></span>|<span data-ttu-id="2c49c-126">管理者が提供またはインポートしたアプリのタイトルです。</span><span class="sxs-lookup"><span data-stu-id="2c49c-126">The admin provided or imported title of the app.</span></span>|
|<span data-ttu-id="2c49c-127">description</span><span class="sxs-lookup"><span data-stu-id="2c49c-127">description</span></span>|<span data-ttu-id="2c49c-128">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-128">String</span></span>|<span data-ttu-id="2c49c-129">アプリの説明。</span><span class="sxs-lookup"><span data-stu-id="2c49c-129">The description of the app.</span></span>|
|<span data-ttu-id="2c49c-130">publisher</span><span class="sxs-lookup"><span data-stu-id="2c49c-130">Publisher</span></span>|<span data-ttu-id="2c49c-131">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-131">String</span></span>|<span data-ttu-id="2c49c-132">アプリの発行元。</span><span class="sxs-lookup"><span data-stu-id="2c49c-132">The name of the app.</span></span>|
|<span data-ttu-id="2c49c-133">largeIcon</span><span class="sxs-lookup"><span data-stu-id="2c49c-133">largeIcon</span></span>|[<span data-ttu-id="2c49c-134">mimeContent</span><span class="sxs-lookup"><span data-stu-id="2c49c-134">MimeContent</span></span>](../resources/intune_apps_mimecontent.md)|<span data-ttu-id="2c49c-135">アプリの詳細に表示され、アイコンのアップロードに使用される大きいアイコン。</span><span class="sxs-lookup"><span data-stu-id="2c49c-135">The large icon, to be displayed in the app details and used for upload of the icon.</span></span>|
|<span data-ttu-id="2c49c-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="2c49c-136">createdDateTime</span></span>|<span data-ttu-id="2c49c-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2c49c-137">DateTimeOffset</span></span>|<span data-ttu-id="2c49c-138">アプリが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="2c49c-138">The date and time when the page was created.</span></span>|
|<span data-ttu-id="2c49c-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="2c49c-139">lastModifiedDateTime</span></span>|<span data-ttu-id="2c49c-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="2c49c-140">DateTimeOffset</span></span>|<span data-ttu-id="2c49c-141">アプリが最後に変更された日時。</span><span class="sxs-lookup"><span data-stu-id="2c49c-141">The date and time when the attachment was last modified.</span></span>|
|<span data-ttu-id="2c49c-142">isFeatured</span><span class="sxs-lookup"><span data-stu-id="2c49c-142">isFeatured</span></span>|<span data-ttu-id="2c49c-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="2c49c-143">Boolean</span></span>|<span data-ttu-id="2c49c-144">アプリが管理者のおすすめとしてマークされたかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="2c49c-144">The value indicating whether the app is marked as featured by the admin.</span></span>|
|<span data-ttu-id="2c49c-145">privacyInformationUrl</span><span class="sxs-lookup"><span data-stu-id="2c49c-145">privacyInformationUrl</span></span>|<span data-ttu-id="2c49c-146">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-146">String</span></span>|<span data-ttu-id="2c49c-147">プライバシーに関する声明の URL。</span><span class="sxs-lookup"><span data-stu-id="2c49c-147">The privacy statement Url.</span></span>|
|<span data-ttu-id="2c49c-148">informationUrl</span><span class="sxs-lookup"><span data-stu-id="2c49c-148">informationUrl</span></span>|<span data-ttu-id="2c49c-149">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-149">String</span></span>|<span data-ttu-id="2c49c-150">詳細情報の URL。</span><span class="sxs-lookup"><span data-stu-id="2c49c-150">The more information Url.</span></span>|
|<span data-ttu-id="2c49c-151">owner</span><span class="sxs-lookup"><span data-stu-id="2c49c-151">owner</span></span>|<span data-ttu-id="2c49c-152">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-152">String</span></span>|<span data-ttu-id="2c49c-153">アプリの所有者。</span><span class="sxs-lookup"><span data-stu-id="2c49c-153">The owner of the timesheet.</span></span>|
|<span data-ttu-id="2c49c-154">developer</span><span class="sxs-lookup"><span data-stu-id="2c49c-154">developer</span></span>|<span data-ttu-id="2c49c-155">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-155">String</span></span>|<span data-ttu-id="2c49c-156">アプリの開発者。</span><span class="sxs-lookup"><span data-stu-id="2c49c-156">The name of the app.</span></span>|
|<span data-ttu-id="2c49c-157">notes</span><span class="sxs-lookup"><span data-stu-id="2c49c-157">notes</span></span>|<span data-ttu-id="2c49c-158">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-158">String</span></span>|<span data-ttu-id="2c49c-159">アプリ用のメモ。</span><span class="sxs-lookup"><span data-stu-id="2c49c-159">Notes for the app.</span></span>|
|<span data-ttu-id="2c49c-160">publishingState</span><span class="sxs-lookup"><span data-stu-id="2c49c-160">publishingState</span></span>|<span data-ttu-id="2c49c-161">String</span><span class="sxs-lookup"><span data-stu-id="2c49c-161">String</span></span>|<span data-ttu-id="2c49c-162">アプリの発行の状態。</span><span class="sxs-lookup"><span data-stu-id="2c49c-162">The publishing state for the app.</span></span> <span data-ttu-id="2c49c-163">アプリが発行されていない限り、アプリを割り当てることができません。</span><span class="sxs-lookup"><span data-stu-id="2c49c-163">The app cannot be assigned unless the app is published.</span></span> <span data-ttu-id="2c49c-164">可能な値は、`notPublished`、`processing`、`published` です。</span><span class="sxs-lookup"><span data-stu-id="2c49c-164">Possible values are: `notPublished`, `processing`, `published`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2c49c-165">関係</span><span class="sxs-lookup"><span data-stu-id="2c49c-165">Relationships</span></span>
|<span data-ttu-id="2c49c-166">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="2c49c-166">Relationship</span></span>|<span data-ttu-id="2c49c-167">型</span><span class="sxs-lookup"><span data-stu-id="2c49c-167">Type</span></span>|<span data-ttu-id="2c49c-168">説明</span><span class="sxs-lookup"><span data-stu-id="2c49c-168">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2c49c-169">categories</span><span class="sxs-lookup"><span data-stu-id="2c49c-169">categories</span></span>|<span data-ttu-id="2c49c-170">[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="2c49c-170">[mobileAppCategory](../resources/intune_apps_mobileappcategory.md) collection</span></span>|<span data-ttu-id="2c49c-171">このアプリのカテゴリのリストです。</span><span class="sxs-lookup"><span data-stu-id="2c49c-171">The list of categories for this app.</span></span>|
|<span data-ttu-id="2c49c-172">assignments</span><span class="sxs-lookup"><span data-stu-id="2c49c-172">assignments</span></span>|<span data-ttu-id="2c49c-173">[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="2c49c-173">[mobileAppAssignment](../resources/intune_apps_mobileappassignment.md) collection</span></span>|<span data-ttu-id="2c49c-174">このモバイル アプリのグループ割り当てのリスト。</span><span class="sxs-lookup"><span data-stu-id="2c49c-174">The list of group assignments for this mobile app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2c49c-175">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="2c49c-175">JSON Representation</span></span>
<span data-ttu-id="2c49c-176">以下は、リソースの JSON 表記です。</span><span class="sxs-lookup"><span data-stu-id="2c49c-176">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileApp",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "publisher": "String",
  "largeIcon": {
    "@odata.type": "microsoft.graph.mimeContent",
    "type": "String",
    "value": "binary"
  },
  "createdDateTime": "String (timestamp)",
  "lastModifiedDateTime": "String (timestamp)",
  "isFeatured": true,
  "privacyInformationUrl": "String",
  "informationUrl": "String",
  "owner": "String",
  "developer": "String",
  "notes": "String",
  "publishingState": "String"
}
```


