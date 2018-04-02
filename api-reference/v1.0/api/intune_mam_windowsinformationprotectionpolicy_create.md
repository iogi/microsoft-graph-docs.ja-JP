# <a name="create-windowsinformationprotectionpolicy"></a><span data-ttu-id="d31a2-101">Create windowsInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="d31a2-101">Create windowsInformationProtectionPolicy</span></span>

> <span data-ttu-id="d31a2-102">**注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d31a2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d31a2-103">新しい [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-103">Create a new [plannerBucket](../resources/intune_mam_windowsinformationprotectionpolicy.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d31a2-104">前提条件</span><span class="sxs-lookup"><span data-stu-id="d31a2-104">Prerequisites</span></span>
<span data-ttu-id="d31a2-p101">この API を呼び出すには、次のいずれかのアクセス許可が必要です。アクセス許可の選択方法などの詳細については、「[アクセス許可](../../../concepts/permissions_reference.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d31a2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d31a2-107">アクセス許可の種類</span><span class="sxs-lookup"><span data-stu-id="d31a2-107">Permission type</span></span>|<span data-ttu-id="d31a2-108">アクセス許可 (特権の大きいものから小さいものへ)</span><span class="sxs-lookup"><span data-stu-id="d31a2-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d31a2-109">委任 (職場または学校アカウント)</span><span class="sxs-lookup"><span data-stu-id="d31a2-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d31a2-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d31a2-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="d31a2-111">委任 (個人用 Microsoft アカウント)</span><span class="sxs-lookup"><span data-stu-id="d31a2-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d31a2-112">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d31a2-112">Not supported.</span></span>|
|<span data-ttu-id="d31a2-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d31a2-113">Application</span></span>|<span data-ttu-id="d31a2-114">サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d31a2-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d31a2-115">HTTP 要求</span><span class="sxs-lookup"><span data-stu-id="d31a2-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/windowsInformationProtectionPolicies
```

## <a name="request-headers"></a><span data-ttu-id="d31a2-116">要求ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d31a2-116">Request headers</span></span>
|<span data-ttu-id="d31a2-117">ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d31a2-117">Header</span></span>|<span data-ttu-id="d31a2-118">値</span><span class="sxs-lookup"><span data-stu-id="d31a2-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d31a2-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d31a2-119">Authorization</span></span>|<span data-ttu-id="d31a2-120">ベアラー &lt;トークン&gt; が必須。</span><span class="sxs-lookup"><span data-stu-id="d31a2-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="d31a2-121">Accept</span><span class="sxs-lookup"><span data-stu-id="d31a2-121">Accept</span></span>|<span data-ttu-id="d31a2-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d31a2-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d31a2-123">要求本文</span><span class="sxs-lookup"><span data-stu-id="d31a2-123">Request body</span></span>
<span data-ttu-id="d31a2-124">要求の本文に、windowsInformationProtectionPolicy オブジェクトの JSON 表現を指定します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-124">In the request body, supply a JSON representation of calendar object.</span></span>

<span data-ttu-id="d31a2-125">次の表に、windowsInformationProtectionPolicy の作成時に必要なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="d31a2-126">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d31a2-126">Property</span></span>|<span data-ttu-id="d31a2-127">型</span><span class="sxs-lookup"><span data-stu-id="d31a2-127">Type</span></span>|<span data-ttu-id="d31a2-128">説明</span><span class="sxs-lookup"><span data-stu-id="d31a2-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d31a2-129">displayName</span><span class="sxs-lookup"><span data-stu-id="d31a2-129">displayName</span></span>|<span data-ttu-id="d31a2-130">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-130">String</span></span>|<span data-ttu-id="d31a2-131">ポリシーの表示名。</span><span class="sxs-lookup"><span data-stu-id="d31a2-131">Policy display name.</span></span> <span data-ttu-id="d31a2-132">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-132">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="d31a2-133">description</span><span class="sxs-lookup"><span data-stu-id="d31a2-133">description</span></span>|<span data-ttu-id="d31a2-134">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-134">String</span></span>|<span data-ttu-id="d31a2-135">ポリシーの説明。</span><span class="sxs-lookup"><span data-stu-id="d31a2-135">The policy's description.</span></span> <span data-ttu-id="d31a2-136">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-136">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="d31a2-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d31a2-137">createdDateTime</span></span>|<span data-ttu-id="d31a2-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d31a2-138">DateTimeOffset</span></span>|<span data-ttu-id="d31a2-139">ポリシーが作成された日時。</span><span class="sxs-lookup"><span data-stu-id="d31a2-139">The date and time when the page was created.</span></span> <span data-ttu-id="d31a2-140">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-140">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="d31a2-141">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d31a2-141">lastModifiedDateTime</span></span>|<span data-ttu-id="d31a2-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d31a2-142">DateTimeOffset</span></span>|<span data-ttu-id="d31a2-143">ポリシーが変更された最終日時。</span><span class="sxs-lookup"><span data-stu-id="d31a2-143">Last time the policy was modified.</span></span> <span data-ttu-id="d31a2-144">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-144">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="d31a2-145">id</span><span class="sxs-lookup"><span data-stu-id="d31a2-145">id</span></span>|<span data-ttu-id="d31a2-146">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-146">String</span></span>|<span data-ttu-id="d31a2-147">エンティティのキー。</span><span class="sxs-lookup"><span data-stu-id="d31a2-147">Name of the entity.</span></span> <span data-ttu-id="d31a2-148">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-148">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="d31a2-149">version</span><span class="sxs-lookup"><span data-stu-id="d31a2-149">version</span></span>|<span data-ttu-id="d31a2-150">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-150">String</span></span>|<span data-ttu-id="d31a2-151">エンティティのバージョン。</span><span class="sxs-lookup"><span data-stu-id="d31a2-151">Version of the entity.</span></span> <span data-ttu-id="d31a2-152">[managedAppPolicy](../resources/intune_mam_managedapppolicy.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-152">Inherited from [managedAppPolicy](../resources/intune_mam_managedapppolicy.md)</span></span>|
|<span data-ttu-id="d31a2-153">enforcementLevel</span><span class="sxs-lookup"><span data-stu-id="d31a2-153">enforcementLevel</span></span>|<span data-ttu-id="d31a2-154">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-154">String</span></span>|<span data-ttu-id="d31a2-155">WIP の実施レベル。サポートされている値の Enum 定義を参照してください ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承。可能な値: `noProtection`、`encryptAndAuditOnly`、`encryptAuditAndPrompt`、`encryptAuditAndBlock`)。</span><span class="sxs-lookup"><span data-stu-id="d31a2-155">WIP enforcement level.See the Enum definition for supported values Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) Possible values are: `noProtection`, `encryptAndAuditOnly`, `encryptAuditAndPrompt`, `encryptAuditAndBlock`.</span></span>|
|<span data-ttu-id="d31a2-156">enterpriseDomain</span><span class="sxs-lookup"><span data-stu-id="d31a2-156">enterpriseDomain</span></span>|<span data-ttu-id="d31a2-157">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-157">String</span></span>|<span data-ttu-id="d31a2-158">プライマリ エンタープライズ ドメイン ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-158">Primary enterprise domain Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-159">enterpriseProtectedDomainNames</span><span class="sxs-lookup"><span data-stu-id="d31a2-159">enterpriseProtectedDomainNames</span></span>|<span data-ttu-id="d31a2-160">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-160">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d31a2-161">保護するエンタープライズ ドメインのリスト ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-161">List of enterprise domains to be protected Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-162">protectionUnderLockConfigRequired</span><span class="sxs-lookup"><span data-stu-id="d31a2-162">protectionUnderLockConfigRequired</span></span>|<span data-ttu-id="d31a2-163">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-163">Boolean</span></span>|<span data-ttu-id="d31a2-164">ロック機能による保護 (pin での暗号化) を構成するかどうかを指定します ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-164">Specifies whether the protection under lock feature (also known as encrypt under pin) should be configured Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-165">dataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="d31a2-165">dataRecoveryCertificate</span></span>|[<span data-ttu-id="d31a2-166">windowsInformationProtectionDataRecoveryCertificate</span><span class="sxs-lookup"><span data-stu-id="d31a2-166">windowsInformationProtectionDataRecoveryCertificate</span></span>](../resources/intune_mam_windowsinformationprotectiondatarecoverycertificate.md)|<span data-ttu-id="d31a2-167">暗号化されたファイルのデータ回復に使用できる回復証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-167">Specifies a recovery certificate that can be used for data recovery of encrypted files.</span></span> <span data-ttu-id="d31a2-168">これは、暗号化ファイル システム (EFS) のデータ回復エージェント (DRA) 証明書と同じです ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-168">This is the same as the data recovery agent(DRA) certificate for encrypting file system(EFS) Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-169">revokeOnUnenrollDisabled</span><span class="sxs-lookup"><span data-stu-id="d31a2-169">revokeOnUnenrollDisabled</span></span>|<span data-ttu-id="d31a2-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-170">Boolean</span></span>|<span data-ttu-id="d31a2-171">このポリシーは、デバイスが管理サービスから登録を解除するときに WIP キーを取り消すかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-171">This policy controls whether to revoke the WIP keys when a device unenrolls from the management service.</span></span> <span data-ttu-id="d31a2-172">1 (キーの取り消しをしない) に設定すると、キーは取り消されず、ユーザーは登録解除後も引き続き保護されたファイルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d31a2-172">If set to 1 (Don't revoke keys), the keys will not be revoked and the user will continue to have access to protected files after unenrollment.</span></span> <span data-ttu-id="d31a2-173">キーが取り消されない場合は、その後、取り消されたファイルのクリーンアップは行われません。</span><span class="sxs-lookup"><span data-stu-id="d31a2-173">If the keys are not revoked, there will be no revoked file cleanup subsequently.</span></span> <span data-ttu-id="d31a2-174">[windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-174">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-175">rightsManagementServicesTemplateId</span><span class="sxs-lookup"><span data-stu-id="d31a2-175">rightsManagementServicesTemplateId</span></span>|<span data-ttu-id="d31a2-176">GUID</span><span class="sxs-lookup"><span data-stu-id="d31a2-176">Guid</span></span>|<span data-ttu-id="d31a2-177">RMS の暗号化に使用する TemplateID GUID。</span><span class="sxs-lookup"><span data-stu-id="d31a2-177">TemplateID GUID to use for RMS encryption.</span></span> <span data-ttu-id="d31a2-178">RMS テンプレートを使用すると、IT 管理者は、RMS で保護されたファイルにアクセスできるユーザーの詳細とアクセスできる期間の詳細を構成することができます ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-178">The RMS template allows the IT admin to configure the details about who has access to RMS-protected file and how long they have access Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-179">azureRightsManagementServicesAllowed</span><span class="sxs-lookup"><span data-stu-id="d31a2-179">azureRightsManagementServicesAllowed</span></span>|<span data-ttu-id="d31a2-180">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-180">Boolean</span></span>|<span data-ttu-id="d31a2-181">WIP 用の Azure RMS の暗号化を許可するかどうかを指定します ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-181">Specifies whether to allow Azure RMS encryption for WIP Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-182">iconsVisible</span><span class="sxs-lookup"><span data-stu-id="d31a2-182">iconsVisible</span></span>|<span data-ttu-id="d31a2-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-183">Boolean</span></span>|<span data-ttu-id="d31a2-184">エクスプローラーでの WIP で保護されたファイルと、スタート メニューのエンタープライズ専用のアプリ タイルについて、アイコンにオーバーレイを追加するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-184">Determines whether overlays are added to icons for WIP protected files in Explorer and enterprise only app tiles in the Start menu.</span></span> <span data-ttu-id="d31a2-185">Windows 10 Version 1703 以降では、この設定は WIP で保護されたアプリのタイトル バーにおける WIP アイコンの可視性も構成します ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-185">Starting in Windows 10, version 1703 this setting also configures the visibility of the WIP icon in the title bar of a WIP-protected app Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-186">protectedApps</span><span class="sxs-lookup"><span data-stu-id="d31a2-186">protectedApps</span></span>|<span data-ttu-id="d31a2-187">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-187">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="d31a2-188">保護されたアプリケーションはエンタープライズ データにアクセスすることができ、これらのアプリケーションによって処理されるデータは暗号化によって保護されます ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-188">Protected applications can access enterprise data and the data handled by those applications are protected with encryption Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-189">exemptApps</span><span class="sxs-lookup"><span data-stu-id="d31a2-189">exemptApps</span></span>|<span data-ttu-id="d31a2-190">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-190">[windowsInformationProtectionApp](../resources/intune_mam_windowsinformationprotectionapp.md) collection</span></span>|<span data-ttu-id="d31a2-191">適用除外アプリケーションはエンタープライズ データにアクセスできますが、これらのアプリケーションによって処理されるデータは保護されません。</span><span class="sxs-lookup"><span data-stu-id="d31a2-191">Exempt applications can also access enterprise data, but the data handled by those applications are not protected.</span></span> <span data-ttu-id="d31a2-192">これは、重要なエンタープライズ アプリケーションの中には、暗号化されたデータとの互換性の問題がある可能性があるためです。</span><span class="sxs-lookup"><span data-stu-id="d31a2-192">This is because some critical enterprise applications may have compatibility problems with encrypted data.</span></span> <span data-ttu-id="d31a2-193">[windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-193">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-194">enterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="d31a2-194">enterpriseNetworkDomainNames</span></span>|<span data-ttu-id="d31a2-195">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-195">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d31a2-196">これは、エンタープライズの境界を構成するドメインのリストです。</span><span class="sxs-lookup"><span data-stu-id="d31a2-196">This is the list of domains that comprise the boundaries of the enterprise.</span></span> <span data-ttu-id="d31a2-197">デバイスに送信されるこれらのドメインの 1 つからのデータは、エンタープライズ データと見なされ、保護されます。これらの場所は、エンタープライズ データを共有するための安全なコピー先と見なされます ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-197">Data from one of these domains that is sent to a device will be considered enterprise data and protected These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-198">enterpriseProxiedDomains</span><span class="sxs-lookup"><span data-stu-id="d31a2-198">enterpriseProxiedDomains</span></span>|<span data-ttu-id="d31a2-199">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-199">[windowsInformationProtectionProxiedDomainCollection](../resources/intune_mam_windowsinformationprotectionproxieddomaincollection.md) collection</span></span>|<span data-ttu-id="d31a2-200">保護が必要な、クラウドでホストされているエンタープライズ リソース ドメインのリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d31a2-200">Contains a list of Enterprise resource domains hosted in the cloud that need to be protected.</span></span> <span data-ttu-id="d31a2-201">これらのリソースへの接続は、エンタープライズ データと見なされます。</span><span class="sxs-lookup"><span data-stu-id="d31a2-201">Connections to these resources are considered enterprise data.</span></span> <span data-ttu-id="d31a2-202">プロキシがクラウド リソースとペアリング済みの場合、クラウド リソースへのトラフィックは、指定されたプロキシ サーバー (ポート 80) を介してエンタープライズ ネットワーク経由でルーティングされます。</span><span class="sxs-lookup"><span data-stu-id="d31a2-202">If a proxy is paired with a cloud resource, traffic to the cloud resource will be routed through the enterprise network via the denoted proxy server (on Port 80).</span></span> <span data-ttu-id="d31a2-203">この目的で使用されるプロキシ サーバーは、EnterpriseInternalProxyServers ポリシーを使用して構成する必要があります ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-203">A proxy server used for this purpose must also be configured using the EnterpriseInternalProxyServers policy Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-204">enterpriseIPRanges</span><span class="sxs-lookup"><span data-stu-id="d31a2-204">enterpriseIPRanges</span></span>|<span data-ttu-id="d31a2-205">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-205">[windowsInformationProtectionIPRangeCollection](../resources/intune_mam_windowsinformationprotectioniprangecollection.md) collection</span></span>|<span data-ttu-id="d31a2-206">エンタープライズ ネットワーク内のコンピューターを定義するエンタープライズ IP の範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-206">Sets the enterprise IP ranges that define the computers in the enterprise network.</span></span> <span data-ttu-id="d31a2-207">これらのコンピューターからのデータはエンタープライズの一部と見なされ、保護されます。</span><span class="sxs-lookup"><span data-stu-id="d31a2-207">Data that comes from those computers will be considered part of the enterprise and protected.</span></span> <span data-ttu-id="d31a2-208">これらの場所は、エンタープライズ データを共有するための安全なコピー先と見なされます ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-208">These locations will be considered a safe destination for enterprise data to be shared to Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-209">enterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d31a2-209">enterpriseIPRangesAreAuthoritative</span></span>|<span data-ttu-id="d31a2-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-210">Boolean</span></span>|<span data-ttu-id="d31a2-211">構成済みのリストを承諾し、ヒューリスティックを使用した他のサブネットの検索を行わないよう、クライアントに指示するブール値。</span><span class="sxs-lookup"><span data-stu-id="d31a2-211">Boolean value that tells the client to accept the configured list and not to use heuristics to attempt to find other subnets.</span></span> <span data-ttu-id="d31a2-212">既定値は false です ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-212">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-213">enterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="d31a2-213">enterpriseProxyServers</span></span>|<span data-ttu-id="d31a2-214">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-214">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d31a2-215">これは、プロキシ サーバーのリストです。</span><span class="sxs-lookup"><span data-stu-id="d31a2-215">This is a list of proxy servers.</span></span> <span data-ttu-id="d31a2-216">このリストにないサーバーは、非エンタープライズと見なされます ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-216">Any server not on this list is considered non-enterprise Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-217">enterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="d31a2-217">enterpriseInternalProxyServers</span></span>|<span data-ttu-id="d31a2-218">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-218">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d31a2-219">これは、内部プロキシ サーバーのコンマ区切りのリストです。</span><span class="sxs-lookup"><span data-stu-id="d31a2-219">This is the comma-separated list of internal proxy servers.</span></span> <span data-ttu-id="d31a2-220">例: "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59"。</span><span class="sxs-lookup"><span data-stu-id="d31a2-220">For example, "157.54.14.28, 157.54.11.118, 10.202.14.167, 157.53.14.163, 157.69.210.59".</span></span> <span data-ttu-id="d31a2-221">これらのプロキシは、管理者により、インターネット上の特定のリソースに接続するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="d31a2-221">These proxies have been configured by the admin to connect to specific resources on the Internet.</span></span> <span data-ttu-id="d31a2-222">それらはエンタープライズ ネットワークの場所にあると見なされます。</span><span class="sxs-lookup"><span data-stu-id="d31a2-222">They are considered to be enterprise network locations.</span></span> <span data-ttu-id="d31a2-223">これらのプロキシは、EnterpriseProxiedDomains ポリシーの構成のみで活用され、これらのプロキシを介して、一致するドメインにトラフィックを強制します ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-223">The proxies are only leveraged in configuring the EnterpriseProxiedDomains policy to force traffic to the matched domains through these proxies Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-224">enterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="d31a2-224">enterpriseProxyServersAreAuthoritative</span></span>|<span data-ttu-id="d31a2-225">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-225">Boolean</span></span>|<span data-ttu-id="d31a2-226">プロキシの構成済みリストを承諾し、他の作業プロキシの検出を試みないよう、クライアントに指示するブール値。</span><span class="sxs-lookup"><span data-stu-id="d31a2-226">Boolean value that tells the client to accept the configured list of proxies and not try to detect other work proxies.</span></span> <span data-ttu-id="d31a2-227">既定値は false です ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-227">Default is false Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-228">neutralDomainResources</span><span class="sxs-lookup"><span data-stu-id="d31a2-228">neutralDomainResources</span></span>|<span data-ttu-id="d31a2-229">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-229">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d31a2-230">職場または個人のリソースに使用できるドメイン名のリスト ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-230">List of domain names that can used for work or personal resource Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-231">indexingEncryptedStoresOrItemsBlocked</span><span class="sxs-lookup"><span data-stu-id="d31a2-231">indexingEncryptedStoresOrItemsBlocked</span></span>|<span data-ttu-id="d31a2-232">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-232">Boolean</span></span>|<span data-ttu-id="d31a2-233">このスイッチは Windows Search Indexer 用で、アイテムのインデックス作成を許可または禁止します ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-233">This switch is for the Windows Search Indexer, to allow or disallow indexing of items Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-234">smbAutoEncryptedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="d31a2-234">smbAutoEncryptedFileExtensions</span></span>|<span data-ttu-id="d31a2-235">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) コレクション</span><span class="sxs-lookup"><span data-stu-id="d31a2-235">[windowsInformationProtectionResourceCollection](../resources/intune_mam_windowsinformationprotectionresourcecollection.md) collection</span></span>|<span data-ttu-id="d31a2-236">企業の境界内で SMB 共有からコピーするときに、当該拡張子を持つファイルが暗号化されるように、ファイル拡張子のリストを指定します ([windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承)</span><span class="sxs-lookup"><span data-stu-id="d31a2-236">Specifies a list of file extensions, so that files with these extensions are encrypted when copying from an SMB share within the corporate boundary Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-237">isAssigned</span><span class="sxs-lookup"><span data-stu-id="d31a2-237">isAssigned</span></span>|<span data-ttu-id="d31a2-238">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-238">Boolean</span></span>|<span data-ttu-id="d31a2-239">包含グループにポリシーを配置するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-239">Indicates if the policy is deployed to any inclusion groups or not.</span></span> <span data-ttu-id="d31a2-240">[windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md) から継承します</span><span class="sxs-lookup"><span data-stu-id="d31a2-240">Inherited from [windowsInformationProtection](../resources/intune_mam_windowsinformationprotection.md)</span></span>|
|<span data-ttu-id="d31a2-241">revokeOnMdmHandoffDisabled</span><span class="sxs-lookup"><span data-stu-id="d31a2-241">revokeOnMdmHandoffDisabled</span></span>|<span data-ttu-id="d31a2-242">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-242">Boolean</span></span>|<span data-ttu-id="d31a2-243">RS2 の新しいプロパティ、保留中のドキュメント</span><span class="sxs-lookup"><span data-stu-id="d31a2-243">New property in RS2, pending documentation</span></span>|
|<span data-ttu-id="d31a2-244">mdmEnrollmentUrl</span><span class="sxs-lookup"><span data-stu-id="d31a2-244">mdmEnrollmentUrl</span></span>|<span data-ttu-id="d31a2-245">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-245">String</span></span>|<span data-ttu-id="d31a2-246">MDM の登録 URL</span><span class="sxs-lookup"><span data-stu-id="d31a2-246">Enrollment url for the MDM</span></span>|
|<span data-ttu-id="d31a2-247">windowsHelloForBusinessBlocked</span><span class="sxs-lookup"><span data-stu-id="d31a2-247">windowsHelloForBusinessBlocked</span></span>|<span data-ttu-id="d31a2-248">Boolean</span><span class="sxs-lookup"><span data-stu-id="d31a2-248">Boolean</span></span>|<span data-ttu-id="d31a2-249">Windows にサインインするためのメソッドとして Windows Hello for Business を設定するブール値です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-249">Boolean value that sets Windows Hello for Business as a method for signing into Windows.</span></span>|
|<span data-ttu-id="d31a2-250">pinMinimumLength</span><span class="sxs-lookup"><span data-stu-id="d31a2-250">pinMinimumLength</span></span>|<span data-ttu-id="d31a2-251">Int32</span><span class="sxs-lookup"><span data-stu-id="d31a2-251">Int32</span></span>|<span data-ttu-id="d31a2-252">PIN に必要な文字の最小数を設定する整数値です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-252">Integer value that sets the minimum number of characters required for the PIN.</span></span> <span data-ttu-id="d31a2-253">既定値は 4 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-253">Default value is 4.</span></span> <span data-ttu-id="d31a2-254">このポリシー設定で構成できる最小値は 4 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-254">The lowest number you can configure for this policy setting is 4.</span></span> <span data-ttu-id="d31a2-255">構成できる最大値は、[PIN の最大文字数] ポリシー設定で構成された値、または 127 のうち、どちらか小さい方です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-255">The largest number you can configure must be less than the number configured in the Maximum PIN length policy setting or the number 127, whichever is the lowest.</span></span>|
|<span data-ttu-id="d31a2-256">pinUppercaseLetters</span><span class="sxs-lookup"><span data-stu-id="d31a2-256">pinUppercaseLetters</span></span>|<span data-ttu-id="d31a2-257">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-257">String</span></span>|<span data-ttu-id="d31a2-258">Windows Hello for Business の PIN における大文字の使用を構成する整数値です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-258">Integer value that configures the use of uppercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="d31a2-259">既定値は NotAllow です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-259">Default is NotAllow.</span></span> <span data-ttu-id="d31a2-260">可能な値は、`notAllow`、`requireAtLeastOne`、`allow` です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-260">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="d31a2-261">pinLowercaseLetters</span><span class="sxs-lookup"><span data-stu-id="d31a2-261">pinLowercaseLetters</span></span>|<span data-ttu-id="d31a2-262">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-262">String</span></span>|<span data-ttu-id="d31a2-263">Windows Hello for Business の PIN における小文字の使用を構成する整数値です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-263">Integer value that configures the use of lowercase letters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="d31a2-264">既定値は NotAllow です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-264">Default is NotAllow.</span></span> <span data-ttu-id="d31a2-265">可能な値は、`notAllow`、`requireAtLeastOne`、`allow` です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-265">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="d31a2-266">pinSpecialCharacters</span><span class="sxs-lookup"><span data-stu-id="d31a2-266">pinSpecialCharacters</span></span>|<span data-ttu-id="d31a2-267">String</span><span class="sxs-lookup"><span data-stu-id="d31a2-267">String</span></span>|<span data-ttu-id="d31a2-268">Windows Hello for Business の PIN における特殊文字の使用を構成する整数値です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-268">Integer value that configures the use of special characters in the Windows Hello for Business PIN.</span></span> <span data-ttu-id="d31a2-269">Windows Hello for Business の PIN ジェスチャの有効な特殊文字は以下のとおりです: !</span><span class="sxs-lookup"><span data-stu-id="d31a2-269">Valid special characters for Windows Hello for Business PIN gestures include: !</span></span> <span data-ttu-id="d31a2-270">" # $ % & ' ( ) \* + , - .</span><span class="sxs-lookup"><span data-stu-id="d31a2-270">" # $ % & ' ( ) \* + , - .</span></span> <span data-ttu-id="d31a2-271">/ : ; < = > ?</span><span class="sxs-lookup"><span data-stu-id="d31a2-271">/ : ; < = > ?</span></span><span data-ttu-id="d31a2-272"> @ \[ \ \] ^ _ \` {</span><span class="sxs-lookup"><span data-stu-id="d31a2-272"> @ \[ \ \] ^ _ \` {</span></span> | <span data-ttu-id="d31a2-273">} ~。</span><span class="sxs-lookup"><span data-stu-id="d31a2-273">=, ==</span></span> <span data-ttu-id="d31a2-274">既定値は NotAllow です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-274">Default is NotAllow.</span></span> <span data-ttu-id="d31a2-275">可能な値は、`notAllow`、`requireAtLeastOne`、`allow` です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-275">Possible values are: `notAllow`, `requireAtLeastOne`, `allow`.</span></span>|
|<span data-ttu-id="d31a2-276">pinExpirationDays</span><span class="sxs-lookup"><span data-stu-id="d31a2-276">pinExpirationDays</span></span>|<span data-ttu-id="d31a2-277">Int32</span><span class="sxs-lookup"><span data-stu-id="d31a2-277">Int32</span></span>|<span data-ttu-id="d31a2-278">この整数値は、システムがユーザーに PIN の変更を要求する前の、PIN の使用可能な期間 (日数) を指定します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-278">Integer value specifies the period of time (in days) that a PIN can be used before the system requires the user to change it.</span></span> <span data-ttu-id="d31a2-279">このポリシー設定で構成できる最大値は 730 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-279">The largest number you can configure for this policy setting is 730.</span></span> <span data-ttu-id="d31a2-280">このポリシー設定で構成できる最小値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-280">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="d31a2-281">このポリシーが 0 に設定されている場合、ユーザーの PIN は期限切れになりません。</span><span class="sxs-lookup"><span data-stu-id="d31a2-281">If this policy is set to 0, then the user's PIN will never expire.</span></span> <span data-ttu-id="d31a2-282">このノードは、Windows 10 バージョン 1511 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="d31a2-282">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="d31a2-283">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-283">Default is 0.</span></span>|
|<span data-ttu-id="d31a2-284">numberOfPastPinsRemembered</span><span class="sxs-lookup"><span data-stu-id="d31a2-284">numberOfPastPinsRemembered</span></span>|<span data-ttu-id="d31a2-285">Int32</span><span class="sxs-lookup"><span data-stu-id="d31a2-285">Int32</span></span>|<span data-ttu-id="d31a2-286">再使用できないユーザー アカウントに関連付けられる過去の PIN の数を指定する整数値です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-286">Integer value that specifies the number of past PINs that can be associated to a user account that can't be reused.</span></span> <span data-ttu-id="d31a2-287">このポリシー設定で構成できる最大値は 50 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-287">The largest number you can configure for this policy setting is 50.</span></span> <span data-ttu-id="d31a2-288">このポリシー設定で構成できる最小値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-288">The lowest number you can configure for this policy setting is 0.</span></span> <span data-ttu-id="d31a2-289">このポリシーが 0 に設定されている場合、以前の PIN の格納は不要です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-289">If this policy is set to 0, then storage of previous PINs is not required.</span></span> <span data-ttu-id="d31a2-290">このノードは、Windows 10 バージョン 1511 で追加されました。</span><span class="sxs-lookup"><span data-stu-id="d31a2-290">This node was added in Windows 10, version 1511.</span></span> <span data-ttu-id="d31a2-291">既定値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-291">Default is 0.</span></span>|
|<span data-ttu-id="d31a2-292">passwordMaximumAttemptCount</span><span class="sxs-lookup"><span data-stu-id="d31a2-292">passwordMaximumAttemptCount</span></span>|<span data-ttu-id="d31a2-293">Int32</span><span class="sxs-lookup"><span data-stu-id="d31a2-293">Int32</span></span>|<span data-ttu-id="d31a2-294">デバイスがワイプされるまでの、許可されている認証失敗の回数です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-294">The number of authentication failures allowed before the device will be wiped.</span></span> <span data-ttu-id="d31a2-295">値を 0 にすると、デバイス ワイプ機能が無効になります。</span><span class="sxs-lookup"><span data-stu-id="d31a2-295">A value of 0 disables device wipe functionality.</span></span> <span data-ttu-id="d31a2-296">範囲は整数 X (デスクトップの場合: 4 <= X <= 16、モバイル デバイスの場合: 0 <= X <= 999) です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-296">Range is an integer X where 4 <= X <= 16 for desktop and 0 <= X <= 999 for mobile devices.</span></span>|
|<span data-ttu-id="d31a2-297">minutesOfInactivityBeforeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="d31a2-297">minutesOfInactivityBeforeDeviceLock</span></span>|<span data-ttu-id="d31a2-298">Int32</span><span class="sxs-lookup"><span data-stu-id="d31a2-298">Int32</span></span>|<span data-ttu-id="d31a2-299">デバイスがアイドルになった後に、デバイスの PIN またはパスワードがロックされるまでの最大時間 (分) を指定します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-299">Specifies the maximum amount of time (in minutes) allowed after the device is idle that will cause the device to become PIN or password locked.</span></span>   <span data-ttu-id="d31a2-300">範囲は整数 X (0 < = X < = 999) です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-300">Range is an integer X where 0 <= X <= 999.</span></span>|
|<span data-ttu-id="d31a2-301">daysWithoutContactBeforeUnenroll</span><span class="sxs-lookup"><span data-stu-id="d31a2-301">daysWithoutContactBeforeUnenroll</span></span>|<span data-ttu-id="d31a2-302">Int32</span><span class="sxs-lookup"><span data-stu-id="d31a2-302">Int32</span></span>|<span data-ttu-id="d31a2-303">アプリのデータがワイプされるまでのオフライン期間 (日数)</span><span class="sxs-lookup"><span data-stu-id="d31a2-303">Offline interval before app data is wiped (days)</span></span> |



## <a name="response"></a><span data-ttu-id="d31a2-304">応答</span><span class="sxs-lookup"><span data-stu-id="d31a2-304">Response</span></span>
<span data-ttu-id="d31a2-305">成功した場合、このメソッドは `201 Created` 応答コードと、応答本文で [windowsInformationProtectionPolicy](../resources/intune_mam_windowsinformationprotectionpolicy.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="d31a2-305">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_mam_windowsinformationprotectionpolicy.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d31a2-306">例</span><span class="sxs-lookup"><span data-stu-id="d31a2-306">Example</span></span>
### <a name="request"></a><span data-ttu-id="d31a2-307">要求</span><span class="sxs-lookup"><span data-stu-id="d31a2-307">Request</span></span>
<span data-ttu-id="d31a2-308">以下は、要求の例です。</span><span class="sxs-lookup"><span data-stu-id="d31a2-308">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/windowsInformationProtectionPolicies
Content-type: application/json
Content-length: 4466

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 0,
  "pinUppercaseLetters": "requireAtLeastOne",
  "pinLowercaseLetters": "requireAtLeastOne",
  "pinSpecialCharacters": "requireAtLeastOne",
  "pinExpirationDays": 1,
  "numberOfPastPinsRemembered": 10,
  "passwordMaximumAttemptCount": 11,
  "minutesOfInactivityBeforeDeviceLock": 3,
  "daysWithoutContactBeforeUnenroll": 0
}
```

### <a name="response"></a><span data-ttu-id="d31a2-309">応答</span><span class="sxs-lookup"><span data-stu-id="d31a2-309">Response</span></span>
<span data-ttu-id="d31a2-p130">以下は、応答の例です。注:簡潔にするために、ここに示す応答オブジェクトは切り詰められている場合があります。すべてのプロパティは実際の呼び出しから返されます。</span><span class="sxs-lookup"><span data-stu-id="d31a2-p130">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4574

{
  "@odata.type": "#microsoft.graph.windowsInformationProtectionPolicy",
  "displayName": "Display Name value",
  "description": "Description value",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "id": "6397be61-be61-6397-61be-976361be9763",
  "version": "Version value",
  "enforcementLevel": "encryptAndAuditOnly",
  "enterpriseDomain": "Enterprise Domain value",
  "enterpriseProtectedDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "protectionUnderLockConfigRequired": true,
  "dataRecoveryCertificate": {
    "@odata.type": "microsoft.graph.windowsInformationProtectionDataRecoveryCertificate",
    "subjectName": "Subject Name value",
    "description": "Description value",
    "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
    "certificate": "Y2VydGlmaWNhdGU="
  },
  "revokeOnUnenrollDisabled": true,
  "rightsManagementServicesTemplateId": "<Unknown Primitive Type Edm.Guid>",
  "azureRightsManagementServicesAllowed": true,
  "iconsVisible": true,
  "protectedApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "exemptApps": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionStoreApp",
      "displayName": "Display Name value",
      "description": "Description value",
      "publisherName": "Publisher Name value",
      "productName": "Product Name value",
      "denied": true
    }
  ],
  "enterpriseNetworkDomainNames": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxiedDomains": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionProxiedDomainCollection",
      "displayName": "Display Name value",
      "proxiedDomains": [
        {
          "@odata.type": "microsoft.graph.proxiedDomain",
          "ipAddressOrFQDN": "Ip Address Or FQDN value",
          "proxy": "Proxy value"
        }
      ]
    }
  ],
  "enterpriseIPRanges": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionIPRangeCollection",
      "displayName": "Display Name value",
      "ranges": [
        {
          "@odata.type": "microsoft.graph.iPv6Range",
          "lowerAddress": "Lower Address value",
          "upperAddress": "Upper Address value"
        }
      ]
    }
  ],
  "enterpriseIPRangesAreAuthoritative": true,
  "enterpriseProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseInternalProxyServers": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "enterpriseProxyServersAreAuthoritative": true,
  "neutralDomainResources": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "indexingEncryptedStoresOrItemsBlocked": true,
  "smbAutoEncryptedFileExtensions": [
    {
      "@odata.type": "microsoft.graph.windowsInformationProtectionResourceCollection",
      "displayName": "Display Name value",
      "resources": [
        "Resources value"
      ]
    }
  ],
  "isAssigned": true,
  "revokeOnMdmHandoffDisabled": true,
  "mdmEnrollmentUrl": "https://example.com/mdmEnrollmentUrl/",
  "windowsHelloForBusinessBlocked": true,
  "pinMinimumLength": 0,
  "pinUppercaseLetters": "requireAtLeastOne",
  "pinLowercaseLetters": "requireAtLeastOne",
  "pinSpecialCharacters": "requireAtLeastOne",
  "pinExpirationDays": 1,
  "numberOfPastPinsRemembered": 10,
  "passwordMaximumAttemptCount": 11,
  "minutesOfInactivityBeforeDeviceLock": 3,
  "daysWithoutContactBeforeUnenroll": 0
}
```


