# <a name="remotelockactionresult-resource-type"></a><span data-ttu-id="535ed-101">remoteLockActionResult リソースの種類</span><span class="sxs-lookup"><span data-stu-id="535ed-101">remoteLockActionResult resource type</span></span>

> <span data-ttu-id="535ed-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="535ed-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="535ed-103">ロック解除するためのピンが含まれるアクション結果のロック。</span><span class="sxs-lookup"><span data-stu-id="535ed-103">Lock action result with a pin to unlock</span></span>

<span data-ttu-id="535ed-104">[deviceActionResult](../resources/intune_devices_deviceactionresult.md) からの継承</span><span class="sxs-lookup"><span data-stu-id="535ed-104">Inherits from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>

## <a name="properties"></a><span data-ttu-id="535ed-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="535ed-105">Properties</span></span>
|<span data-ttu-id="535ed-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="535ed-106">Property</span></span>|<span data-ttu-id="535ed-107">型</span><span class="sxs-lookup"><span data-stu-id="535ed-107">Type</span></span>|<span data-ttu-id="535ed-108">説明</span><span class="sxs-lookup"><span data-stu-id="535ed-108">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="535ed-109">actionName</span><span class="sxs-lookup"><span data-stu-id="535ed-109">ActionName</span></span>|<span data-ttu-id="535ed-110">文字列型 (String)</span><span class="sxs-lookup"><span data-stu-id="535ed-110">String</span></span>|<span data-ttu-id="535ed-111">[deviceActionResult](../resources/intune_devices_deviceactionresult.md) から継承されるアクション名</span><span class="sxs-lookup"><span data-stu-id="535ed-111">Action name Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="535ed-112">actionState</span><span class="sxs-lookup"><span data-stu-id="535ed-112">actionState</span></span>|<span data-ttu-id="535ed-113">文字列型 (String)</span><span class="sxs-lookup"><span data-stu-id="535ed-113">String</span></span>|<span data-ttu-id="535ed-114">[deviceActionResult](../resources/intune_devices_deviceactionresult.md) から継承されるアクションの状態。可能な値: `none`、`pending`、`canceled`、`active`、`done`、`failed`、`notSupported`。</span><span class="sxs-lookup"><span data-stu-id="535ed-114">State of the action Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md) Possible values are: `none`, `pending`, `canceled`, `active`, `done`, `failed`, `notSupported`.</span></span>|
|<span data-ttu-id="535ed-115">startDateTime</span><span class="sxs-lookup"><span data-stu-id="535ed-115">startDateTime</span></span>|<span data-ttu-id="535ed-116">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="535ed-116">DateTimeOffset</span></span>|<span data-ttu-id="535ed-117">アクションが開始された時刻。[deviceActionResult](../resources/intune_devices_deviceactionresult.md) から継承。</span><span class="sxs-lookup"><span data-stu-id="535ed-117">Time the action was initiated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="535ed-118">lastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="535ed-118">lastUpdatedDateTime</span></span>|<span data-ttu-id="535ed-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="535ed-119">DateTimeOffset</span></span>|<span data-ttu-id="535ed-120">アクション状態の最終更新時刻。[deviceActionResult](../resources/intune_devices_deviceactionresult.md) から継承</span><span class="sxs-lookup"><span data-stu-id="535ed-120">Time the action state was last updated Inherited from [deviceActionResult](../resources/intune_devices_deviceactionresult.md)</span></span>|
|<span data-ttu-id="535ed-121">unlockPin</span><span class="sxs-lookup"><span data-stu-id="535ed-121">unlockPin</span></span>|<span data-ttu-id="535ed-122">文字列型 (String)</span><span class="sxs-lookup"><span data-stu-id="535ed-122">String</span></span>|<span data-ttu-id="535ed-123">クライアントをロック解除するためのピン</span><span class="sxs-lookup"><span data-stu-id="535ed-123">Pin to unlock the client</span></span>|

## <a name="relationships"></a><span data-ttu-id="535ed-124">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="535ed-124">Relationships</span></span>
<span data-ttu-id="535ed-125">なし</span><span class="sxs-lookup"><span data-stu-id="535ed-125">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="535ed-126">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="535ed-126">JSON Representation</span></span>
<span data-ttu-id="535ed-127">以下は、リソースの JSON 表記です。</span><span class="sxs-lookup"><span data-stu-id="535ed-127">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.remoteLockActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.remoteLockActionResult",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)",
  "unlockPin": "String"
}
```


