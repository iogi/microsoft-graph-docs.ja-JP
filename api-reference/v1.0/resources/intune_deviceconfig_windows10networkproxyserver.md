# <a name="windows10networkproxyserver-resource-type"></a><span data-ttu-id="e3343-101">windows10NetworkProxyServer リソースの種類</span><span class="sxs-lookup"><span data-stu-id="e3343-101">windows10NetworkProxyServer resource type</span></span>

> <span data-ttu-id="e3343-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3343-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3343-103">ネットワーク プロキシ サーバーのポリシーです。</span><span class="sxs-lookup"><span data-stu-id="e3343-103">Network Proxy Server Policy.</span></span>
## <a name="properties"></a><span data-ttu-id="e3343-104">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3343-104">Properties</span></span>
|<span data-ttu-id="e3343-105">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3343-105">Property</span></span>|<span data-ttu-id="e3343-106">型</span><span class="sxs-lookup"><span data-stu-id="e3343-106">Type</span></span>|<span data-ttu-id="e3343-107">説明</span><span class="sxs-lookup"><span data-stu-id="e3343-107">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e3343-108">address</span><span class="sxs-lookup"><span data-stu-id="e3343-108">address</span></span>|<span data-ttu-id="e3343-109">String</span><span class="sxs-lookup"><span data-stu-id="e3343-109">String</span></span>|<span data-ttu-id="e3343-110">プロキシ サーバーへのアドレス。</span><span class="sxs-lookup"><span data-stu-id="e3343-110">Address to the proxy server.</span></span> <span data-ttu-id="e3343-111"><server>\[“:”<port>\] 形式でアドレスを指定します</span><span class="sxs-lookup"><span data-stu-id="e3343-111">Specify an address in the format <server>\[“:”<port>\]</span></span>|
|<span data-ttu-id="e3343-112">exceptions</span><span class="sxs-lookup"><span data-stu-id="e3343-112">exceptions</span></span>|<span data-ttu-id="e3343-113">String コレクション</span><span class="sxs-lookup"><span data-stu-id="e3343-113">String collection</span></span>|<span data-ttu-id="e3343-114">プロキシ サーバーを使用できないアドレス。</span><span class="sxs-lookup"><span data-stu-id="e3343-114">Addresses that should not use the proxy server.</span></span> <span data-ttu-id="e3343-115">システムは、このノードで指定されたもので始まるアドレスに対してプロキシ サーバーを使用しません。</span><span class="sxs-lookup"><span data-stu-id="e3343-115">The system will not use the proxy server for addresses beginning with what is specified in this node.</span></span>|
|<span data-ttu-id="e3343-116">useForLocalAddresses</span><span class="sxs-lookup"><span data-stu-id="e3343-116">useForLocalAddresses</span></span>|<span data-ttu-id="e3343-117">Boolean</span><span class="sxs-lookup"><span data-stu-id="e3343-117">Boolean</span></span>|<span data-ttu-id="e3343-118">ローカル (イントラネット) アドレスにプロキシ サーバーを使用する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e3343-118">Specifies whether the proxy server should be used for local (intranet) addresses.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e3343-119">リレーションシップ</span><span class="sxs-lookup"><span data-stu-id="e3343-119">Relationships</span></span>
<span data-ttu-id="e3343-120">なし</span><span class="sxs-lookup"><span data-stu-id="e3343-120">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e3343-121">JSON 表記</span><span class="sxs-lookup"><span data-stu-id="e3343-121">JSON Representation</span></span>
<span data-ttu-id="e3343-122">以下は、リソースの JSON 表記です。</span><span class="sxs-lookup"><span data-stu-id="e3343-122">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10NetworkProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10NetworkProxyServer",
  "address": "String",
  "exceptions": [
    "String"
  ],
  "useForLocalAddresses": true
}
```


