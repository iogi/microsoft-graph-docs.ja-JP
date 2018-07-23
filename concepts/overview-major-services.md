# <a name="major-services-and-features-in-microsoft-graph"></a><span data-ttu-id="3f290-101">Microsoft Graph の主要なサービスおよび機能</span><span class="sxs-lookup"><span data-stu-id="3f290-101">Major services and features in Microsoft Graph</span></span>

<span data-ttu-id="3f290-102">Microsoft Graph を使用すると、非常に優れた Office 365、Windows 10、および Microsoft 365 のエンタープライズ モビリティおよびセキュリティのサービスを統合することができます。</span><span class="sxs-lookup"><span data-stu-id="3f290-102">Microsoft Graph enables you to integrate with the best of Office 365, Windows 10, and Enterprise Mobility and Security services in Microsoft 365.</span></span> <span data-ttu-id="3f290-103">さらに、ユーザーの生産性、創造性、チーム共同作業を促進し、ビジネス リソースおよびユーザー データを保護することのできるセキュリティおよびソーシャル インテリジェンスが提供されます。</span><span class="sxs-lookup"><span data-stu-id="3f290-103">Additionally, it offers security and social intelligence that can boost user productivity, creativity, and team collaboration, and protect business resources and users' data.</span></span> 

## <a name="users-and-groups"></a><span data-ttu-id="3f290-104">ユーザーとグループ</span><span class="sxs-lookup"><span data-stu-id="3f290-104">Users and groups</span></span>

<span data-ttu-id="3f290-105">Microsoft Graph の中心となるのは、ユーザーおよびグループの概念です。</span><span class="sxs-lookup"><span data-stu-id="3f290-105">At the core of Microsoft Graph are the concepts of the user and group.</span></span> 

<span data-ttu-id="3f290-106">Microsoft Graph の_ユーザー_は、Microsoft 365 クラウド サービスを使用する何百万人のうちの 1 人です。</span><span class="sxs-lookup"><span data-stu-id="3f290-106">A _user_ in Microsoft Graph is one among the millions who use Microsoft 365 cloud services.</span></span> <span data-ttu-id="3f290-107">これは、ID が保護され、アクセスが的確に管理されるフォーカル ポイントです。</span><span class="sxs-lookup"><span data-stu-id="3f290-107">It is the focal point whose identity is protected and access is well managed.</span></span> <span data-ttu-id="3f290-108">ユーザーのデータは、ビジネスを推進する力となるものです。</span><span class="sxs-lookup"><span data-stu-id="3f290-108">The user's data is what drives businesses.</span></span> <span data-ttu-id="3f290-109">Microsoft Graph サービスによりそのデータが、豊富なコンテキスト、リアルタイムの更新、および深い洞察において企業から利用可能になり、しかも常に適切な許可によってのみ利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3f290-109">Microsoft Graph services makes this data available to businesses in rich contexts, real-time updates, and deep insights, and, always only with the appropriate permissions.</span></span>

<span data-ttu-id="3f290-110">Office 365 の_グループ_は、ユーザーが共同作業を実行するための基本的なエンティティです。</span><span class="sxs-lookup"><span data-stu-id="3f290-110">An Office 365 _group_ is the fundamental entity that lets users collaborate.</span></span> <span data-ttu-id="3f290-111">これは、他のサービスと統合して、タスク計画、共同作業、教育などにおいて豊富なシナリオが可能になります。</span><span class="sxs-lookup"><span data-stu-id="3f290-111">It integrates with other services, enabling richer scenarios in task planning, teamwork, education, and more.</span></span> 

|<span data-ttu-id="3f290-112">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-112">Feature</span></span>     |<span data-ttu-id="3f290-113">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-113">Supporting services</span></span>  |<span data-ttu-id="3f290-114">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-114">Description</span></span> |<span data-ttu-id="3f290-115">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-115">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-116">ユーザー</span><span class="sxs-lookup"><span data-stu-id="3f290-116">Users</span></span> | <span data-ttu-id="3f290-117">Azure AD および生産性向上、コラボレーション、インテリジェンス、および教育機関向けの多くのサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-117">Azure AD and most productivity, collaboration, intelligence, and education services</span></span> | <span data-ttu-id="3f290-118">ユーザーは、Microsoft Graph の中心となるものであり、多くの Microsoft Graph サービスは、ユーザー中心の機能を構築します。</span><span class="sxs-lookup"><span data-stu-id="3f290-118">The user is a core focus of Microsoft Graph, around which many Microsoft Graph services build user-centric functionality.</span></span> | [<span data-ttu-id="3f290-119">Microsoft Graph でのユーザーの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-119">Overview of users in Microsoft Graph</span></span>](../concepts/azuread-users-concept-overview.md)|
|<span data-ttu-id="3f290-120">グループ</span><span class="sxs-lookup"><span data-stu-id="3f290-120">Groups</span></span> | <span data-ttu-id="3f290-121">Azure AD、OneDrive、OneNote、Outlook、Planner</span><span class="sxs-lookup"><span data-stu-id="3f290-121">Azure AD, OneDrive, OneNote, Outlook, Planner</span></span> | <span data-ttu-id="3f290-122">Office 365 グループは、ユーザーが会話、ファイル、メモ、予定表、プランなどを共有するための基本コラボレーション単位を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f290-122">An Office 365 group provides the fundamental collaborative unit for users to share conversations, files, notes, calendar, plans, and more.</span></span> | [<span data-ttu-id="3f290-123">Microsoft Graph での Office 365 グループの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-123">Overview of Office 365 groups in Microsoft Graph</span></span>](../concepts/office365-groups-concept-overview.md) |

## <a name="connecting-users-data-microsoft-365-services-and-your-apps"></a><span data-ttu-id="3f290-124">ユーザーのデータ、Microsoft 365 サービス、およびアプリの接続</span><span class="sxs-lookup"><span data-stu-id="3f290-124">Connecting users' data, Microsoft 365 services, and your apps</span></span>

<span data-ttu-id="3f290-125">中心となるユーザーおよびグループを始めとして、Microsoft Graph は、広範囲に及ぶシナリオをサポートするためのデータを管理、保護、および抽出する Microsoft 365 のサービスと機能のネットワークを形成します。</span><span class="sxs-lookup"><span data-stu-id="3f290-125">Starting with users and groups at the core, Microsoft Graph forms a network of Microsoft 365 services and features that manage, protect, and extract data to support a wide range of scenarios.</span></span> <span data-ttu-id="3f290-126">Microsoft Graph により、当人の承認を尊重しながら、豊富なユーザー データにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="3f290-126">Microsoft Graph lets you access this wealth of user data while always respecting proper authorization.</span></span>

![Microsoft Graph からユーザーのデータに接続する](images/microsoft-graph-connects-users-data.png)

### <a name="services-and-features"></a><span data-ttu-id="3f290-128">サービスと機能</span><span class="sxs-lookup"><span data-stu-id="3f290-128">Excel Services and Business Intelligence features</span></span>

<span data-ttu-id="3f290-129">Microsoft Graph の一部のサービスは、そこで初めて登場したサービスであり、その他のサービスはスタンドアロン サービスとして知られており、現在 Microsoft Graph に収束しています。</span><span class="sxs-lookup"><span data-stu-id="3f290-129">Some services in Microsoft Graph make their debut there, others have been well-known as standalone services and are now converging in Microsoft Graph.</span></span> <span data-ttu-id="3f290-130">その API セットは、「[Microsoft REST API ガイドライン](https://github.com/Microsoft/api-guidelines)」で詳細が示されている合理化デザインに従うものであり、Microsoft Graph REST の単一エンドポイントによってアクセス可能になっています。`https://graph.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="3f290-130">Their API sets follow a streamlined design as detailed in the [Microsoft REST API guidelines](https://github.com/Microsoft/api-guidelines), and are now accessible through the single Microsoft Graph REST endpoint `https://graph.microsoft.com`.</span></span> <span data-ttu-id="3f290-131">この記事の残りの部分では、主要なサービスと機能をカテゴリ別に一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="3f290-131">The rest of this article lists the major services and features by category.</span></span> 


## <a name="identity-and-access-management"></a><span data-ttu-id="3f290-132">ID およびアクセス管理</span><span class="sxs-lookup"><span data-stu-id="3f290-132">Identity and access management</span></span>

|<span data-ttu-id="3f290-133">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-133">Feature</span></span>     |<span data-ttu-id="3f290-134">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-134">Supporting services</span></span>  |<span data-ttu-id="3f290-135">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-135">Description</span></span> |<span data-ttu-id="3f290-136">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-136">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-137">ID およびアクセス管理</span><span class="sxs-lookup"><span data-stu-id="3f290-137">Identity and access management</span></span> | <span data-ttu-id="3f290-138">Azure AD</span><span class="sxs-lookup"><span data-stu-id="3f290-138">Azure AD</span></span> | <span data-ttu-id="3f290-139">ユーザー、グループ、およびアプリケーションなどのディレクトリ リソースを作成したり管理したりします。</span><span class="sxs-lookup"><span data-stu-id="3f290-139">Creates and manages directory resources such as users, groups, and applications.</span></span> <span data-ttu-id="3f290-140">リソースおよびデータへのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="3f290-140">Manages access to resources and data.</span></span> | [<span data-ttu-id="3f290-141">Azure AD ID およびアクセス管理の概要</span><span class="sxs-lookup"><span data-stu-id="3f290-141">Azure AD identity and access management overview</span></span>](../concepts/azuread-identity-access-management-concept-overview.md)  |


## <a name="productivity"></a><span data-ttu-id="3f290-142">生産性</span><span class="sxs-lookup"><span data-stu-id="3f290-142">Productivity</span></span>

|<span data-ttu-id="3f290-143">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-143">Feature</span></span>     |<span data-ttu-id="3f290-144">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-144">Supporting services</span></span>  |<span data-ttu-id="3f290-145">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-145">Description</span></span> |<span data-ttu-id="3f290-146">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-146">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-147">予定表</span><span class="sxs-lookup"><span data-stu-id="3f290-147">Calendar</span></span> | <span data-ttu-id="3f290-148">Outlook</span><span class="sxs-lookup"><span data-stu-id="3f290-148">Outlook</span></span>  | <span data-ttu-id="3f290-149">ユーザーが、Web、モバイル、およびデスクトップ デバイスの上で予定と会議を設定することができるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-149">Lets users set up appointments and meetings on the web, mobile and desktop devices.</span></span> <span data-ttu-id="3f290-150">これは、Office 365 の中の Outlook メッセージング通信ハブの一部であり、それにより、ユーザーはメールと連絡先を管理することができます。</span><span class="sxs-lookup"><span data-stu-id="3f290-150">It is part of the Outlook messaging communication hub in Office 365 that also lets users manage emails and contacts.</span></span> | [<span data-ttu-id="3f290-151">Outlook カレンダーの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-151">Outlook calendar overview</span></span>](../concepts/outlook-calendar-concept-overview.md)  |
| <span data-ttu-id="3f290-152">ファイル</span><span class="sxs-lookup"><span data-stu-id="3f290-152">Files</span></span> | <span data-ttu-id="3f290-153">OneDrive と SharePoint</span><span class="sxs-lookup"><span data-stu-id="3f290-153">OneDrive for Business and SharePoint</span></span> | <span data-ttu-id="3f290-154">OneDrive および SharePoint でユーザー ファイルを管理および共有します。</span><span class="sxs-lookup"><span data-stu-id="3f290-154">Manages and shares user files on OneDrive and SharePoint.</span></span> | [<span data-ttu-id="3f290-155">OneDrive ファイル ストレージの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-155">OneDrive files storage overview</span></span>](../concepts/onedrive-concept-overview.md) |
| <span data-ttu-id="3f290-156">メール</span><span class="sxs-lookup"><span data-stu-id="3f290-156">Mail</span></span> | <span data-ttu-id="3f290-157">Outlook</span><span class="sxs-lookup"><span data-stu-id="3f290-157">Outlook</span></span> | <span data-ttu-id="3f290-158">ユーザーが、ワークフローの中で、Web、モバイル、およびデスクトップ デバイス上で、通信したり、メッセージを整理したり、優先順位を管理したりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-158">Lets users communicate, organize messages, and manage priorities in their workflows, on the web, mobile and desktop devices.</span></span> <span data-ttu-id="3f290-159">これは、Office 365 の中の Outlook 通信ハブの一部であり、それにより、ユーザーは連絡先を管理したり、会議をスケジューリングしたりできます。</span><span class="sxs-lookup"><span data-stu-id="3f290-159">It is part of the Outlook communication hub in Office 365 that also lets users manage contacts and schedule meetings.</span></span> | [<span data-ttu-id="3f290-160">Outlook メールの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-160">Outlook mail overview</span></span>](../concepts/outlook-mail-concept-overview.md) |
| <span data-ttu-id="3f290-161">メモ</span><span class="sxs-lookup"><span data-stu-id="3f290-161">Notes</span></span> | <span data-ttu-id="3f290-162">OneNote</span><span class="sxs-lookup"><span data-stu-id="3f290-162">OneNote</span></span> | <span data-ttu-id="3f290-163">ユーザーが、アイデアと情報を計画したり整理したりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-163">Lets users plan and organize ideas and information.</span></span> | [<span data-ttu-id="3f290-164">OneNote ノートの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-164">OneNote notes overview</span></span>](../concepts/integrate_with_onenote.md) |
| <span data-ttu-id="3f290-165">個人用連絡先</span><span class="sxs-lookup"><span data-stu-id="3f290-165">Personal contacts</span></span> | <span data-ttu-id="3f290-166">Outlook</span><span class="sxs-lookup"><span data-stu-id="3f290-166">Outlook</span></span> | <span data-ttu-id="3f290-167">Web、モバイル、およびデスクトップ デバイス上での連絡先マネージャー。</span><span class="sxs-lookup"><span data-stu-id="3f290-167">Contacts manager on the web, mobile and desktop devices.</span></span> <span data-ttu-id="3f290-168">これは、Office 365 の中の Outlook メッセージング通信ハブの一部であり、それにより、ユーザーはメールを管理したり、会議をスケジューリングしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="3f290-168">It is part of the Outlook messaging communication hub in Office 365 that also lets users manage emails and schedule meetings.</span></span>  | [<span data-ttu-id="3f290-169">Outlook 個人用連絡先の概要</span><span class="sxs-lookup"><span data-stu-id="3f290-169">Outlook personal contacts overview</span></span>](../concepts/outlook-contacts-concept-overview.md) |
| <span data-ttu-id="3f290-170">ブックとグラフ</span><span class="sxs-lookup"><span data-stu-id="3f290-170">Workbooks and charts</span></span> | <span data-ttu-id="3f290-171">Excel</span><span class="sxs-lookup"><span data-stu-id="3f290-171">Excel</span></span> | <span data-ttu-id="3f290-172">ユーザーが Excel のスプレッドシートを使用して、複雑な計算を実行したり、データを追跡、分析、および視覚化したり、本格的なレポートを生成したりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-172">Lets users use Excel spreadsheets to do complex calculations, track, analyze, and visualize data, and generate professional reports.</span></span> | [<span data-ttu-id="3f290-173">Excel のブックとグラフの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-173">Excel workbooks and charts overview</span></span>](../concepts/excel-concept-overview.md) |


## <a name="collaboration"></a><span data-ttu-id="3f290-174">グループ作業</span><span class="sxs-lookup"><span data-stu-id="3f290-174">Collaboration</span></span>

<!-- Want to update links to concept overviews as they are created over time. 
-->
|<span data-ttu-id="3f290-175">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-175">Feature</span></span>     |<span data-ttu-id="3f290-176">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-176">Supporting services</span></span>  |<span data-ttu-id="3f290-177">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-177">Description</span></span> |<span data-ttu-id="3f290-178">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-178">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-179">サイトとリスト</span><span class="sxs-lookup"><span data-stu-id="3f290-179">Sites and lists</span></span>  | <span data-ttu-id="3f290-180">SharePoint</span><span class="sxs-lookup"><span data-stu-id="3f290-180">SharePoint</span></span> | <span data-ttu-id="3f290-181">ユーザーおよび Office 365 グループがコンテンツ (リスト、ファイル、ノートを含む) を共有、整理、管理、および検出するための Web ベースのプラットフォーム。</span><span class="sxs-lookup"><span data-stu-id="3f290-181">Web-based platform for users and Office 365 groups to share, organize, manage, and discover content (including lists, files, and notes).</span></span> | [<span data-ttu-id="3f290-182">SharePoint のサイトおよびコンテンツの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-182">SharePoint sites and content overview</span></span>](../concepts/sharepoint-concept-overview.md) | 
|<span data-ttu-id="3f290-183">タスクとプラン</span><span class="sxs-lookup"><span data-stu-id="3f290-183">Tasks and plans</span></span> | <span data-ttu-id="3f290-184">Planner</span><span class="sxs-lookup"><span data-stu-id="3f290-184">Planner</span></span> | <span data-ttu-id="3f290-185">Office 365 グループ内のユーザーがプランを作成したり、タスクを割り当てたり、進捗状況を追跡したりできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-185">Enables users in Office 365 groups to create plans, assign tasks, and track progress.</span></span> | [<span data-ttu-id="3f290-186">Planner のプランとタスクの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-186">Planner plans and tasks overview</span></span>](../concepts/planner-concept-overview.md) |
|<span data-ttu-id="3f290-187">チームワーク (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3f290-187">Teamwork (preview)</span></span> |  <span data-ttu-id="3f290-188">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="3f290-188">14. Microsoft Teams apps</span></span> | <span data-ttu-id="3f290-189">チームがファイル、ノート、予定表、およびプランを共有するための、デジタル ハブおよびチャット ベースのワークスペース。</span><span class="sxs-lookup"><span data-stu-id="3f290-189">Digital hub and chat-based workspace for teams to share files, notes, calendar, and plans.</span></span> | [<span data-ttu-id="3f290-190">Microsoft Teams のチームワークの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-190">Microsoft Teams teamwork overview</span></span>](../concepts/teams-concept-overview.md) |


## <a name="social-intelligence-and-analytics"></a><span data-ttu-id="3f290-191">ソーシャル インテリジェンスおよび分析機能</span><span class="sxs-lookup"><span data-stu-id="3f290-191">Social intelligence and analytics</span></span>

|<span data-ttu-id="3f290-192">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-192">Feature</span></span>     |<span data-ttu-id="3f290-193">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-193">Supporting services</span></span>  |<span data-ttu-id="3f290-194">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-194">Description</span></span> |<span data-ttu-id="3f290-195">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-195">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-196">ソーシャル インテリジェンス: 連絡先</span><span class="sxs-lookup"><span data-stu-id="3f290-196">Social intelligence: people</span></span> | <span data-ttu-id="3f290-197">Azure AD、Outlook、SharePoint など</span><span class="sxs-lookup"><span data-stu-id="3f290-197">Azure AD, Outlook, SharePoint, and more</span></span> | <span data-ttu-id="3f290-198">ユーザーの通信や共同作業のパターン、またビジネスの付き合いによって決まるユーザーとの関連性に応じて連絡先についての情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f290-198">Gets information about persons as ordered by their relevance to a user, determined by the user's communication and collaboration patterns, and business relationships.</span></span>  | [<span data-ttu-id="3f290-199">Microsoft Graph でのソーシャル インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="3f290-199">Social intelligence in Microsoft Graph</span></span>](../concepts/social-intel-concept-overview.md) |
| <span data-ttu-id="3f290-200">ソーシャル インテリジェンス: ドキュメントのインサイト (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3f290-200">Social intelligence: document insights (preview)</span></span> | <span data-ttu-id="3f290-201">Delve、OneDrive、Outlook、SharePoint</span><span class="sxs-lookup"><span data-stu-id="3f290-201">Delve, OneDrive, Outlook, SharePoint</span></span> | <span data-ttu-id="3f290-202">高度な分析機能と機械学習のテクニックを使用して、よく使用されるドキュメントやユーザーが表示、変更、または共有したドキュメントを取得します。</span><span class="sxs-lookup"><span data-stu-id="3f290-202">Uses advanced analytics and machine learning techniques to get documents trending around, viewed, modified, or shared by a user.</span></span>  | [<span data-ttu-id="3f290-203">Microsoft Graph でのソーシャル インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="3f290-203">Social intelligence in Microsoft Graph</span></span>](../concepts/social-intel-concept-overview.md)  |


## <a name="device-management"></a><span data-ttu-id="3f290-204">デバイスの管理</span><span class="sxs-lookup"><span data-stu-id="3f290-204">Device management</span></span>

|<span data-ttu-id="3f290-205">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-205">Feature</span></span>     |<span data-ttu-id="3f290-206">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-206">Supporting services</span></span>  |<span data-ttu-id="3f290-207">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-207">Description</span></span> |<span data-ttu-id="3f290-208">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-208">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
|<span data-ttu-id="3f290-209">デバイスとアプリ</span><span class="sxs-lookup"><span data-stu-id="3f290-209">Devices and apps</span></span> | <span data-ttu-id="3f290-210">Intune</span><span class="sxs-lookup"><span data-stu-id="3f290-210">Intune</span></span> | <span data-ttu-id="3f290-211">デバイスを登録および構成し、組織内でモバイル アプリケーション管理します。</span><span class="sxs-lookup"><span data-stu-id="3f290-211">Enrolls and configures devices, and manages mobile applications in your organization.</span></span> | [<span data-ttu-id="3f290-212">Intune のデバイスとアプリの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-212">Intune devices and apps overview</span></span>](../concepts/intune-concept-overview.md) |


## <a name="security"></a><span data-ttu-id="3f290-213">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="3f290-213">Security</span></span>

|<span data-ttu-id="3f290-214">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-214">Feature</span></span>     |<span data-ttu-id="3f290-215">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-215">Supporting services</span></span>  |<span data-ttu-id="3f290-216">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-216">Description</span></span> |<span data-ttu-id="3f290-217">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-217">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-218">セキュリティ統合 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3f290-218">Security integration (preview)</span></span> | <span data-ttu-id="3f290-219">Azure AD Identity Protection、Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="3f290-219">Azure AD Identity Protection, Azure Security Center</span></span> | <span data-ttu-id="3f290-220">Microsoft およびエコシステムのパートナーを通じて、セキュリティのインサイトやアクションに対する統一ゲートウェイを提供します。</span><span class="sxs-lookup"><span data-stu-id="3f290-220">Provides a unified gateway to security insights and actions across Microsoft and ecosystem partners.</span></span> | [<span data-ttu-id="3f290-221">Microsoft Graph のセキュリティ</span><span class="sxs-lookup"><span data-stu-id="3f290-221">SharePoint in Microsoft Graph</span></span>](../concepts/security-concept-overview.md) |
| <span data-ttu-id="3f290-222">Identity Protection (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3f290-222">Identity protection (preview)</span></span> | <span data-ttu-id="3f290-223">Azure AD</span><span class="sxs-lookup"><span data-stu-id="3f290-223">Azure AD</span></span> | <span data-ttu-id="3f290-224">Azure AD 内のユーザーのためにサインインおよびアカウント リスク データへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="3f290-224">Gives access to sign-in and account risk data for users in Azure AD.</span></span> | [<span data-ttu-id="3f290-225">Microsoft Graph のセキュリティ</span><span class="sxs-lookup"><span data-stu-id="3f290-225">SharePoint in Microsoft Graph</span></span>](../concepts/security-concept-overview.md)  |



## <a name="cross-device-experiences"></a><span data-ttu-id="3f290-226">クロスデバイス エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="3f290-226">Cross-device experiences</span></span>

|<span data-ttu-id="3f290-227">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-227">Feature</span></span>     |<span data-ttu-id="3f290-228">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-228">Supporting services</span></span>  |<span data-ttu-id="3f290-229">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-229">Description</span></span> |<span data-ttu-id="3f290-230">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-230">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-231">クロスデバイス エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="3f290-231">Cross-device experiences</span></span> | <span data-ttu-id="3f290-232">アクティビティ フィード、デバイスの中継</span><span class="sxs-lookup"><span data-stu-id="3f290-232">Activity feed, device relay</span></span> | <span data-ttu-id="3f290-233">単一デバイスを超えて、種類やプラットフォームに関係なくデバイスからデバイスへユーザーと共に移行できるアプリ エクスペリエンスを可能にします。</span><span class="sxs-lookup"><span data-stu-id="3f290-233">Enables app experiences that transcend a single device, and instead move with the user from device to device regardless of its type and platform.</span></span> | [<span data-ttu-id="3f290-234">クロスデバイス エクスペリエンスの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-234">Overview for cross-device experiences</span></span>](../concepts/cross-device-concept-overview.md) |


## <a name="usage-reports"></a><span data-ttu-id="3f290-235">利用状況レポート</span><span class="sxs-lookup"><span data-stu-id="3f290-235">Usage reports</span></span>

|<span data-ttu-id="3f290-236">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-236">Feature</span></span>     |<span data-ttu-id="3f290-237">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-237">Supporting services</span></span>  |<span data-ttu-id="3f290-238">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-238">Description</span></span> |<span data-ttu-id="3f290-239">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-239">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-240">レポート</span><span class="sxs-lookup"><span data-stu-id="3f290-240">Reports</span></span> | <span data-ttu-id="3f290-241">Microsoft Teams、OneDrive、Outlook、SharePoint、Skype for Business、Yammer</span><span class="sxs-lookup"><span data-stu-id="3f290-241">Microsoft Teams, OneDrive, Outlook, SharePoint, Skype for Business, Yammer</span></span> | <span data-ttu-id="3f290-242">サポート サービスのアクティビティおよび使用状況の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="3f290-242">Gets activity and usage information of a supporting service.</span></span> | [<span data-ttu-id="3f290-243">使用状況レポートの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-243">Usage reports overview</span></span>](../concepts/reportroot-concept-overview.md) |


## <a name="education"></a><span data-ttu-id="3f290-244">教育</span><span class="sxs-lookup"><span data-stu-id="3f290-244">Education permissions</span></span>

|<span data-ttu-id="3f290-245">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-245">Feature</span></span>     |<span data-ttu-id="3f290-246">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-246">Supporting services</span></span>  |<span data-ttu-id="3f290-247">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-247">Description</span></span> |<span data-ttu-id="3f290-248">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-248">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-249">教育</span><span class="sxs-lookup"><span data-stu-id="3f290-249">Education permissions</span></span> | <span data-ttu-id="3f290-250">Azure AD、教育</span><span class="sxs-lookup"><span data-stu-id="3f290-250">Azure AD, Education</span></span> | <span data-ttu-id="3f290-251">学校、クラス、学生、教師、および割り当て情報など、教育機関向けシナリオに関連する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3f290-251">Provides information relevant for education scenarios, including schools, classes, students, teachers, and assignment info.</span></span> <span data-ttu-id="3f290-252">ISV が、教師の作業時間を短縮し、チームワークとコラボレーションを促進する教室用のアプリケーションをビルドできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-252">Enables ISVs to build applications for the classroom that save teachers time and promote teamwork and collaboration.</span></span>  | [<span data-ttu-id="3f290-253">教育機関向けの概要</span><span class="sxs-lookup"><span data-stu-id="3f290-253">Education overview</span></span>](../concepts/education-concept-overview.md) |


## <a name="business-applications"></a><span data-ttu-id="3f290-254">ビジネス アプリケーション</span><span class="sxs-lookup"><span data-stu-id="3f290-254">Business applications</span></span>

|<span data-ttu-id="3f290-255">機能</span><span class="sxs-lookup"><span data-stu-id="3f290-255">Feature</span></span>     |<span data-ttu-id="3f290-256">サポートするサービス</span><span class="sxs-lookup"><span data-stu-id="3f290-256">Supporting services</span></span>  |<span data-ttu-id="3f290-257">説明</span><span class="sxs-lookup"><span data-stu-id="3f290-257">Description</span></span> |<span data-ttu-id="3f290-258">詳細情報</span><span class="sxs-lookup"><span data-stu-id="3f290-258">More information</span></span> |
|:-----------|:--------------------|:-----------|:----------------|
| <span data-ttu-id="3f290-259">顧客の予約 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="3f290-259">Customer booking (preview)</span></span> | <span data-ttu-id="3f290-260">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="3f290-260">Microsoft Bookings</span></span> | <span data-ttu-id="3f290-261">小規模企業を対象として、顧客が Web または Facebook 上で直接にサービスを予約できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-261">Targets small businesses to enable their customers to book services directly on the web or Facebook.</span></span> <span data-ttu-id="3f290-262">業務担当者が、顧客の好み、サービスと価格、スタッフのリストとスケジュール、その他の一般的なビジネス情報を管理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f290-262">Lets business operators manage customer preferences, services and pricing, staff lists and schedules, and other common business information.</span></span> | [<span data-ttu-id="3f290-263">Microsoft Bookings API の概要</span><span class="sxs-lookup"><span data-stu-id="3f290-263">Microsoft Bookings API overview</span></span>](../concepts/booking-concept-overview.md) |


## <a name="next-steps"></a><span data-ttu-id="3f290-264">次の手順</span><span class="sxs-lookup"><span data-stu-id="3f290-264">Next steps</span></span>

<!-- Need to update the destination page titles and URLs as Matt's v-team finalize on the examples and featured scenarios content 
-->

- <span data-ttu-id="3f290-265">実際の顧客の問題を解決する、Microsoft Graph のサービスに基づいて構築されたクリエイティブなソリューションの[例](https://developer.microsoft.com/ja-JP/graph/examples)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3f290-265">See [examples](https://developer.microsoft.com/ja-JP/graph/examples) of creative solutions built on top of services in Microsoft Graph that solve real customer problems.</span></span>
- <span data-ttu-id="3f290-266">目次の「**詳細情報**」を見て、さまざまなシナリオで使用できるサービスや機能についての詳細情報を参照します _。_</span><span class="sxs-lookup"><span data-stu-id="3f290-266">Look under **Learn** in the table of contents to read about services and features that _you_ can use in your scenarios.</span></span>
- <span data-ttu-id="3f290-267">[Graph エクスプローラー](https://developer.microsoft.com/graph/graph-explorer)でサンプルの要求を試します。</span><span class="sxs-lookup"><span data-stu-id="3f290-267">Try a sample request in the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer).</span></span>
- <span data-ttu-id="3f290-268">[クイック スタート](https://developer.microsoft.com/graph/quick-start)を使用して、すぐに実行できるサンプル アプリをセットアップします。</span><span class="sxs-lookup"><span data-stu-id="3f290-268">Use the [quick start](https://developer.microsoft.com/graph/quick-start) to set up a ready-to-run sample app.</span></span>