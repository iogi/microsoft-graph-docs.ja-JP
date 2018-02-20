# <a name="ioshomescreenapp-resource-type"></a><span data-ttu-id="05d29-101">iosHomeScreenApp リソースの種類</span><span class="sxs-lookup"><span data-stu-id="05d29-101">iosHomeScreenApp resource type</span></span>

> <span data-ttu-id="05d29-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="05d29-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="05d29-103">ホーム画面上のアプリのアイコンを表します</span><span class="sxs-lookup"><span data-stu-id="05d29-103">Represents an icon for an app on the Home Screen</span></span>

<span data-ttu-id="05d29-104">[iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md) からの継承</span><span class="sxs-lookup"><span data-stu-id="05d29-104">Inherits from [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span></span>

## <a name="properties"></a><span data-ttu-id="05d29-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="05d29-105">Properties</span></span>
|<span data-ttu-id="05d29-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="05d29-106">Property</span></span>|<span data-ttu-id="05d29-107">型</span><span class="sxs-lookup"><span data-stu-id="05d29-107">Type</span></span>|<span data-ttu-id="05d29-108">説明</span><span class="sxs-lookup"><span data-stu-id="05d29-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="05d29-109">displayName</span><span class="sxs-lookup"><span data-stu-id="05d29-109">displayName</span></span>|<span data-ttu-id="05d29-110">文字列型 (String)</span><span class="sxs-lookup"><span data-stu-id="05d29-110">String</span></span>|<span data-ttu-id="05d29-111">アプリの名前。[iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md) から継承</span><span class="sxs-lookup"><span data-stu-id="05d29-111">Name of the app Inherited from [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span></span>|
|<span data-ttu-id="05d29-112">bundleID</span><span class="sxs-lookup"><span data-stu-id="05d29-112">bundleID</span></span>|<span data-ttu-id="05d29-113">文字列型 (String)</span><span class="sxs-lookup"><span data-stu-id="05d29-113">String</span></span>|<span data-ttu-id="05d29-114">アプリの BundleID</span><span class="sxs-lookup"><span data-stu-id="05d29-114">BundleID of app</span></span>|

## <a name="relationships"></a><span data-ttu-id="05d29-115">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="05d29-115">Relationships</span></span>
<span data-ttu-id="05d29-116">なし</span><span class="sxs-lookup"><span data-stu-id="05d29-116">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="05d29-117">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="05d29-117">JSON Representation</span></span>
<span data-ttu-id="05d29-118">以下は、リソースの JSON 表記です。</span><span class="sxs-lookup"><span data-stu-id="05d29-118">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosHomeScreenApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosHomeScreenApp",
  "displayName": "String",
  "bundleID": "String"
}
```


