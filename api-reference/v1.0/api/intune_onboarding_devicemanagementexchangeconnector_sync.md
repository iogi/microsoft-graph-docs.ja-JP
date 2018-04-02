# <a name="sync-action"></a><span data-ttu-id="2c85b-101">sync アクション</span><span class="sxs-lookup"><span data-stu-id="2c85b-101">sync action</span></span>

> <span data-ttu-id="2c85b-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2c85b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2c85b-103">まだ文書化されていません</span><span class="sxs-lookup"><span data-stu-id="2c85b-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2c85b-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="2c85b-104">Prerequisites</span></span>
<span data-ttu-id="2c85b-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2c85b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2c85b-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="2c85b-107">Permission type</span></span>|<span data-ttu-id="2c85b-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="2c85b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2c85b-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="2c85b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2c85b-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2c85b-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="2c85b-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="2c85b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2c85b-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2c85b-112">Not supported.</span></span>|
|<span data-ttu-id="2c85b-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="2c85b-113">Application</span></span>|<span data-ttu-id="2c85b-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2c85b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2c85b-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="2c85b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}/sync
```

## <a name="request-headers"></a><span data-ttu-id="2c85b-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="2c85b-116">Request headers</span></span>
|<span data-ttu-id="2c85b-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="2c85b-117">Header</span></span>|<span data-ttu-id="2c85b-118">値</span><span class="sxs-lookup"><span data-stu-id="2c85b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2c85b-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2c85b-119">Authorization</span></span>|<span data-ttu-id="2c85b-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="2c85b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="2c85b-121">Accept</span><span class="sxs-lookup"><span data-stu-id="2c85b-121">Accept</span></span>|<span data-ttu-id="2c85b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2c85b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2c85b-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="2c85b-123">Request body</span></span>
<span data-ttu-id="2c85b-124">要求本文で、パラメーターの JSON 表記を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c85b-124">In the request body, supply a JSON representation of the Contact object.</span></span>

<span data-ttu-id="2c85b-125">次の表に、このアクションで使用できるパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="2c85b-125">The following table shows the parameters that can be used with this action.</span></span>

|<span data-ttu-id="2c85b-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="2c85b-126">Property</span></span>|<span data-ttu-id="2c85b-127">型</span><span class="sxs-lookup"><span data-stu-id="2c85b-127">Type</span></span>|<span data-ttu-id="2c85b-128">説明</span><span class="sxs-lookup"><span data-stu-id="2c85b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2c85b-129">syncType</span><span class="sxs-lookup"><span data-stu-id="2c85b-129">syncType</span></span>|<span data-ttu-id="2c85b-130">String</span><span class="sxs-lookup"><span data-stu-id="2c85b-130">String</span></span>|<span data-ttu-id="2c85b-131">実行される同期の種類。完全同期またはデルタ同期のどちらかです。</span><span class="sxs-lookup"><span data-stu-id="2c85b-131">The type of sync which will be executed, full sync or delta sync.</span></span>|



## <a name="response"></a><span data-ttu-id="2c85b-132">応答</span><span class="sxs-lookup"><span data-stu-id="2c85b-132">Response</span></span>
<span data-ttu-id="2c85b-133">成功した場合、このアクションは `204 No Content` 応答コードを返します。</span><span class="sxs-lookup"><span data-stu-id="2c85b-133">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="2c85b-134">例</span><span class="sxs-lookup"><span data-stu-id="2c85b-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="2c85b-135">要求</span><span class="sxs-lookup"><span data-stu-id="2c85b-135">Request</span></span>
<span data-ttu-id="2c85b-136">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="2c85b-136">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/exchangeConnectors/{deviceManagementExchangeConnectorId}/sync

Content-type: application/json
Content-length: 31

{
  "syncType": "deltaSync"
}
```

### <a name="response"></a><span data-ttu-id="2c85b-137">応答</span><span class="sxs-lookup"><span data-stu-id="2c85b-137">Response</span></span>
<span data-ttu-id="2c85b-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="2c85b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```


