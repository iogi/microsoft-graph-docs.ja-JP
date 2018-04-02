# <a name="list-macosgeneraldeviceconfigurations"></a><span data-ttu-id="edbd8-101">macOSGeneralDeviceConfigurations のリスト</span><span class="sxs-lookup"><span data-stu-id="edbd8-101">List macOSGeneralDeviceConfigurations</span></span>

> <span data-ttu-id="edbd8-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="edbd8-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="edbd8-103">[macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) オブジェクトのプロパティとリレーションシップをリストします。</span><span class="sxs-lookup"><span data-stu-id="edbd8-103">List properties and relationships of the [macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="edbd8-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="edbd8-104">Prerequisites</span></span>
<span data-ttu-id="edbd8-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="edbd8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="edbd8-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="edbd8-107">Permission type</span></span>|<span data-ttu-id="edbd8-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="edbd8-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="edbd8-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="edbd8-109">Delegated (work or school account)</span></span>|<span data-ttu-id="edbd8-110">DeviceManagementConfiguration.ReadWrite.All、DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="edbd8-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="edbd8-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="edbd8-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="edbd8-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edbd8-112">Not supported.</span></span>|
|<span data-ttu-id="edbd8-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="edbd8-113">Application</span></span>|<span data-ttu-id="edbd8-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="edbd8-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="edbd8-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="edbd8-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="edbd8-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="edbd8-116">Request headers</span></span>
|<span data-ttu-id="edbd8-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="edbd8-117">Header</span></span>|<span data-ttu-id="edbd8-118">値</span><span class="sxs-lookup"><span data-stu-id="edbd8-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="edbd8-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="edbd8-119">Authorization</span></span>|<span data-ttu-id="edbd8-120">ベアラー &lt;トークン&gt; が必要です。</span><span class="sxs-lookup"><span data-stu-id="edbd8-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="edbd8-121">Accept</span><span class="sxs-lookup"><span data-stu-id="edbd8-121">Accept</span></span>|<span data-ttu-id="edbd8-122">application/json</span><span class="sxs-lookup"><span data-stu-id="edbd8-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="edbd8-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="edbd8-123">Request body</span></span>
<span data-ttu-id="edbd8-124">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="edbd8-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="edbd8-125">応答</span><span class="sxs-lookup"><span data-stu-id="edbd8-125">Response</span></span>
<span data-ttu-id="edbd8-126">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [macOSGeneralDeviceConfiguration](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) オブジェクトのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="edbd8-126">If successful, this method returns a `200 OK` response code and collection of [groupSettingTemplate](../resources/intune_deviceconfig_macosgeneraldeviceconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="edbd8-127">例</span><span class="sxs-lookup"><span data-stu-id="edbd8-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="edbd8-128">要求</span><span class="sxs-lookup"><span data-stu-id="edbd8-128">Request</span></span>
<span data-ttu-id="edbd8-129">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="edbd8-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="edbd8-130">応答</span><span class="sxs-lookup"><span data-stu-id="edbd8-130">Response</span></span>
<span data-ttu-id="edbd8-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="edbd8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1227

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSGeneralDeviceConfiguration",
      "id": "dc356aee-6aee-dc35-ee6a-35dcee6a35dc",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "compliantAppsList": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "compliantAppListType": "appsInListCompliant",
      "emailInDomainSuffixes": [
        "Email In Domain Suffixes value"
      ],
      "passwordBlockSimple": true,
      "passwordExpirationDays": 6,
      "passwordMinimumCharacterSetCount": 0,
      "passwordMinimumLength": 5,
      "passwordMinutesOfInactivityBeforeLock": 5,
      "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
      "passwordPreviousPasswordBlockCount": 2,
      "passwordRequiredType": "alphanumeric",
      "passwordRequired": true
    }
  ]
}
```


