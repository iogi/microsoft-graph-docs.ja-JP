# <a name="get-windows10endpointprotectionconfiguration"></a><span data-ttu-id="7308f-101">Get windows10EndpointProtectionConfiguration</span><span class="sxs-lookup"><span data-stu-id="7308f-101">Get windows10EndpointProtectionConfiguration</span></span>

> <span data-ttu-id="7308f-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7308f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7308f-103">[windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) オブジェクトのプロパティとリレーションシップを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="7308f-103">Read properties and relationships of [plannerBucket](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7308f-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="7308f-104">Prerequisites</span></span>
<span data-ttu-id="7308f-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7308f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7308f-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="7308f-107">Permission type</span></span>|<span data-ttu-id="7308f-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="7308f-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7308f-109">委任 (職場または学校のアカウント)</span><span class="sxs-lookup"><span data-stu-id="7308f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7308f-110">DeviceManagementConfiguration.ReadWrite.All、DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="7308f-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="7308f-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="7308f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7308f-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7308f-112">Not supported.</span></span>|
|<span data-ttu-id="7308f-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="7308f-113">Application</span></span>|<span data-ttu-id="7308f-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7308f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7308f-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="7308f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="7308f-116">オプションのクエリ パラメーター</span><span class="sxs-lookup"><span data-stu-id="7308f-116">Optional query parameters</span></span>
<span data-ttu-id="7308f-117">このメソッドは、応答をカスタマイズするための [OData クエリ パラメーター](https://developer.microsoft.com/ja-JP/graph/docs/overview/query_parameters)をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7308f-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/ja-JP/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7308f-118">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="7308f-118">Request headers</span></span>
|<span data-ttu-id="7308f-119">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="7308f-119">Header</span></span>|<span data-ttu-id="7308f-120">値</span><span class="sxs-lookup"><span data-stu-id="7308f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7308f-121">承認</span><span class="sxs-lookup"><span data-stu-id="7308f-121">Authorization</span></span>|<span data-ttu-id="7308f-122">ベアラー &lt;トークン&gt;が必須。</span><span class="sxs-lookup"><span data-stu-id="7308f-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="7308f-123">承諾</span><span class="sxs-lookup"><span data-stu-id="7308f-123">Accept</span></span>|<span data-ttu-id="7308f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7308f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7308f-125">要求本文</span><span class="sxs-lookup"><span data-stu-id="7308f-125">Request body</span></span>
<span data-ttu-id="7308f-126">このメソッドには、要求本文を指定しません。</span><span class="sxs-lookup"><span data-stu-id="7308f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7308f-127">応答</span><span class="sxs-lookup"><span data-stu-id="7308f-127">Response</span></span>
<span data-ttu-id="7308f-128">成功した場合、このメソッドは `200 OK` 応答コードと、応答本文で [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="7308f-128">If successful, this method returns a `200 OK` response code and a [section](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7308f-129">例</span><span class="sxs-lookup"><span data-stu-id="7308f-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="7308f-130">要求</span><span class="sxs-lookup"><span data-stu-id="7308f-130">Request</span></span>
<span data-ttu-id="7308f-131">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="7308f-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="7308f-132">応答</span><span class="sxs-lookup"><span data-stu-id="7308f-132">Response</span></span>
<span data-ttu-id="7308f-p102">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="7308f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4628

{
  "value": {
    "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
    "id": "09709403-9403-0970-0394-700903947009",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "firewallBlockStatefulFTP": true,
    "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
    "firewallPreSharedKeyEncodingMethod": "none",
    "firewallIPSecExemptionsAllowNeighborDiscovery": true,
    "firewallIPSecExemptionsAllowICMP": true,
    "firewallIPSecExemptionsAllowRouterDiscovery": true,
    "firewallIPSecExemptionsAllowDHCP": true,
    "firewallCertificateRevocationListCheckMethod": "none",
    "firewallMergeKeyingModuleSettings": true,
    "firewallPacketQueueingMethod": "disabled",
    "firewallProfileDomain": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
      "stealthModeBlocked": true,
      "incomingTrafficBlocked": true,
      "unicastResponsesToMulticastBroadcastsBlocked": true,
      "inboundNotificationsBlocked": true,
      "authorizedApplicationRulesFromGroupPolicyMerged": true,
      "globalPortRulesFromGroupPolicyMerged": true,
      "connectionSecurityRulesFromGroupPolicyMerged": true,
      "outboundConnectionsBlocked": true,
      "inboundConnectionsBlocked": true,
      "securedPacketExemptionAllowed": true,
      "policyRulesFromGroupPolicyMerged": true
    },
    "firewallProfilePublic": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
      "stealthModeBlocked": true,
      "incomingTrafficBlocked": true,
      "unicastResponsesToMulticastBroadcastsBlocked": true,
      "inboundNotificationsBlocked": true,
      "authorizedApplicationRulesFromGroupPolicyMerged": true,
      "globalPortRulesFromGroupPolicyMerged": true,
      "connectionSecurityRulesFromGroupPolicyMerged": true,
      "outboundConnectionsBlocked": true,
      "inboundConnectionsBlocked": true,
      "securedPacketExemptionAllowed": true,
      "policyRulesFromGroupPolicyMerged": true
    },
    "firewallProfilePrivate": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
      "stealthModeBlocked": true,
      "incomingTrafficBlocked": true,
      "unicastResponsesToMulticastBroadcastsBlocked": true,
      "inboundNotificationsBlocked": true,
      "authorizedApplicationRulesFromGroupPolicyMerged": true,
      "globalPortRulesFromGroupPolicyMerged": true,
      "connectionSecurityRulesFromGroupPolicyMerged": true,
      "outboundConnectionsBlocked": true,
      "inboundConnectionsBlocked": true,
      "securedPacketExemptionAllowed": true,
      "policyRulesFromGroupPolicyMerged": true
    },
    "defenderAttackSurfaceReductionExcludedPaths": [
      "Defender Attack Surface Reduction Excluded Paths value"
    ],
    "defenderGuardedFoldersAllowedAppPaths": [
      "Defender Guarded Folders Allowed App Paths value"
    ],
    "defenderAdditionalGuardedFolders": [
      "Defender Additional Guarded Folders value"
    ],
    "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
    "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
    "defenderSecurityCenterBlockExploitProtectionOverride": true,
    "appLockerApplicationControl": "enforceComponentsAndStoreApps",
    "smartScreenEnableInShell": true,
    "smartScreenBlockOverrideForFiles": true,
    "applicationGuardEnabled": true,
    "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
    "applicationGuardBlockNonEnterpriseContent": true,
    "applicationGuardAllowPersistence": true,
    "applicationGuardForceAuditing": true,
    "applicationGuardBlockClipboardSharing": "blockBoth",
    "applicationGuardAllowPrintToPDF": true,
    "applicationGuardAllowPrintToXPS": true,
    "applicationGuardAllowPrintToLocalPrinters": true,
    "applicationGuardAllowPrintToNetworkPrinters": true,
    "bitLockerDisableWarningForOtherDiskEncryption": true,
    "bitLockerEnableStorageCardEncryptionOnMobile": true,
    "bitLockerEncryptDevice": true,
    "bitLockerRemovableDrivePolicy": {
      "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
      "encryptionMethod": "aesCbc256",
      "requireEncryptionForWriteAccess": true,
      "blockCrossOrganizationWriteAccess": true
    }
  }
}
```


