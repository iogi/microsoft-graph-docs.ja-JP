# <a name="outlook-mail-api-overview"></a><span data-ttu-id="334bd-101">Outlook メール API の概要</span><span class="sxs-lookup"><span data-stu-id="334bd-101">Outlook mail API overview</span></span>

<span data-ttu-id="334bd-102">Outlook は、Office 365 のメッセージング通信ハブです。</span><span class="sxs-lookup"><span data-stu-id="334bd-102">Outlook is a messaging communication hub in Office 365.</span></span> <span data-ttu-id="334bd-103">これにより、連絡先の管理、会議のスケジュール管理、組織内のユーザーに関する情報の検索、オンライン会話の開始、ファイルの共有、およびグループでの共同作業をすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-103">It also lets you manage contacts, schedule meetings, find information about users in an organization, initiate online conversations, share files, and collaborate in groups.</span></span>

## <a name="why-integrate-with-outlook-mail"></a><span data-ttu-id="334bd-104">Outlook メールと統合する理由</span><span class="sxs-lookup"><span data-stu-id="334bd-104">Why integrate with Outlook mail?</span></span>

### <a name="integrate-with-rich-features-and-reach-hundreds-of-millions-of-customers"></a><span data-ttu-id="334bd-105">豊富な機能を統合して何億というユーザーに達する</span><span class="sxs-lookup"><span data-stu-id="334bd-105">Integrate with rich features and reach hundreds of millions of customers</span></span>

<span data-ttu-id="334bd-106">Outlook を統合するなら、多くのユーザーの好む豊かなエクスペリエンスを取り入れることになります。それは、メール、[連絡先](outlook-contacts-concept-overview.md)、[予定表](outlook-calendar-concept-overview.md)のための直感的で一貫したエクスペリエンスであり、モバイル、Web、およびデスクトップのどのデバイス上でも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="334bd-106">Integrating with Outlook means tapping into the rich experience that customers love - consistent, intuitive experience for mail, [contacts](outlook-contacts-concept-overview.md), [calendar](outlook-calendar-concept-overview.md), available on all devices - mobile, web, and desktop.</span></span>

<span data-ttu-id="334bd-107">[Microsoft Graph](overview.md) を使用することにより、アプリを 1 回だけ作成することにより Outlook と統合することができ、Outlook をメール クライアントとして選んでいる何億人という消費者、何千万という組織ユーザーに達することができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-107">Using [Microsoft Graph](overview.md), you can integrate with Outlook by writing an app just once and reach more than hundreds of millions of consumers, and tens of millions of organization customers who choose Outlook as their email client.</span></span> <span data-ttu-id="334bd-108">メール シナリオを中心としたアプリを作成したり、Outlook および 非 Outlook の他のリレーションシップ、リソース、およびインテリジェンスの宝庫に接続したり、Microsoft クラウドによってサポートされるシナリオを実現したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-108">You can write apps that focus on mail scenarios, or connect to a wealth of other Outlook and non-Outlook relationships, resources, and intelligence, and realize scenarios supported by the Microsoft cloud.</span></span>

### <a name="automate-message-organization-and-processing"></a><span data-ttu-id="334bd-109">メッセージの整理と処理を自動化する</span><span class="sxs-lookup"><span data-stu-id="334bd-109">Automate message organization and processing</span></span>

<span data-ttu-id="334bd-110">多くのユーザーは、Outlook で情報を整理するのを好んでいます。</span><span class="sxs-lookup"><span data-stu-id="334bd-110">Customers like how Outlook help them stay organized.</span></span> <span data-ttu-id="334bd-111">Microsoft Graph により、それらの機能をアプリ開発者が利用することができ、情報の発見作業を最適化し、効率や生産性を向上させるユーザー ワークフローを構築することができます:</span><span class="sxs-lookup"><span data-stu-id="334bd-111">Microsoft Graph brings these features to app developers, enabling them to build customer workflows that optimize on discovery and improve efficiency and productivity:</span></span> 

- <span data-ttu-id="334bd-112">ユーザーは、さまざまな方法でメッセージを整理できます。メッセージを全部受信トレイに入れたまま検索する人もいれば、複数のフォルダーにメッセージを分類保存する人もいます。</span><span class="sxs-lookup"><span data-stu-id="334bd-112">Customers organize their messages in different ways - some leave all messages in the Inbox and simply search for them, others file their messsages in folders.</span></span> <span data-ttu-id="334bd-113">フラットな整理方法とフォルダー ベースの整理方法の両方をサポートする Outlook の柔軟で直感的なアプローチがユーザーに好まれています。</span><span class="sxs-lookup"><span data-stu-id="334bd-113">They like Outlook's flexible and intuitive approach that supports both flat and folder-based organizations.</span></span> <span data-ttu-id="334bd-114">アプリでは、特定のフォルダー内のメッセージまたはユーザーのメールボックス全体のメッセージに対して[フィルター処理、検索、またはソート](query_parameters.md)を便利に実行することができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-114">Apps can conveniently [filter, search, or sort](query_parameters.md) messages in specific folders or the user's entire mailbox.</span></span>

- <span data-ttu-id="334bd-115">Outlook では、名前と色によってカテゴリが区別されます。</span><span class="sxs-lookup"><span data-stu-id="334bd-115">Outlook categories are differentiated by name and color.</span></span> <span data-ttu-id="334bd-116">カテゴリを利用することによりユーザーは、メッセージにタグを付けて、整理や情報発見の作業をさらに便利なものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-116">Categories allow customers to tag messages to enhance organization and discovery.</span></span> <span data-ttu-id="334bd-117">アプリでは、[ユーザーのカテゴリ マスター リストにアクセスしたり定義したり](../api-reference/v1.0/api/outlookuser_post_mastercategories.md)できます。</span><span class="sxs-lookup"><span data-stu-id="334bd-117">Apps can access and [define a user's master list of categories](../api-reference/v1.0/api/outlookuser_post_mastercategories.md).</span></span> <span data-ttu-id="334bd-118">さらにそのリストは、Outlook のメッセージ、またイベント、連絡先、タスク、およびグループ投稿を通じて共有され、アプリ開発者にとってクリエイティブなシナリオの可能性をもたらします。</span><span class="sxs-lookup"><span data-stu-id="334bd-118">More, that list is shared across Outlook messages, as well as events, contacts, tasks, and group posts, and opens up creative scenarios for app developers.</span></span> <span data-ttu-id="334bd-119">たとえば、オンライン研修業者であれば、電子メール、コース イベント、およびフォローアップ課題を、ユーザーが登録しているコースごとに色分けすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-119">For example, an online training provider can color-code the emails, course events, and follow-up assignments for each course a user has enrolled in.</span></span>

- <span data-ttu-id="334bd-120">さらに、アプリのユーザーは、メッセージ (あるいは、イベントまたはタスク) の重要度を変更したり、メッセージにフォローアップ用のフラグを付けたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-120">Additionally, app users can change the importance of a message (or event or task), or flag a message for follow-up.</span></span> <span data-ttu-id="334bd-121">(現時点で Microsoft Graph のフラグの機能は[プレビュー段階](versioning_and_support.md#beta-version)です。)</span><span class="sxs-lookup"><span data-stu-id="334bd-121">(Flagging is currently [in preview](versioning_and_support.md#beta-version) in Microsoft Graph.)</span></span>

- <span data-ttu-id="334bd-122">ルール API を利用すれば、メッセージの整理がさらに上のレベルになります。</span><span class="sxs-lookup"><span data-stu-id="334bd-122">The rules API takes message organization to the next level.</span></span> <span data-ttu-id="334bd-123">アプリでは、[受信トレイ ルール](../api-reference/v1.0/resources/messagerule.md)をセットアップすることにより、受信メッセージを迅速に処理し、メールが乱雑な状態になるのを軽減できます。</span><span class="sxs-lookup"><span data-stu-id="334bd-123">Apps can set up [Inbox rules](../api-reference/v1.0/resources/messagerule.md) to promptly handle incoming messages and reduce email clutter.</span></span> <span data-ttu-id="334bd-124">たとえば、アプリにより、メッセージの件名に特定のキーワードが含まれている場合にメッセージを別のフォルダーに移動したり、後でそれに対応する作業を容易にするためにカテゴリや重要度を割り当てたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-124">For example, an app can automatically move messages to another folder if their subject lines contain certain keywords, and assign categories and importance to make them easier for later follow-up.</span></span>

### <a name="write-smarter-apps-that-leverage-intelligence"></a><span data-ttu-id="334bd-125">インテリジェンスを活用した高度なアプリを作成する</span><span class="sxs-lookup"><span data-stu-id="334bd-125">Write smarter apps that leverage intelligence</span></span> 

<span data-ttu-id="334bd-126">Microsoft Graph を利用することにより、アプリ ユーザーに対してコンテキスト データを提案することができます:</span><span class="sxs-lookup"><span data-stu-id="334bd-126">Use Microsoft Graph to suggest contextual data to your app users:</span></span>

- <span data-ttu-id="334bd-127">[優先受信トレイ](../api-reference/v1.0/resources/manage_focused_inbox.md)および [@ メンション (プレビュー)](../api-reference/beta/api/message_get.md#request-2) を統合し、アプリ ユーザーが気になっているものを最初に読み、返信できるようにする。</span><span class="sxs-lookup"><span data-stu-id="334bd-127">Integrate with [Focused Inbox](../api-reference/v1.0/resources/manage_focused_inbox.md) and [@-mentions (preview)](../api-reference/beta/api/message_get.md#request-2) and let your app users read and respond to what's relevant to them first.</span></span> 

- <span data-ttu-id="334bd-128">メッセージ作成中に[メール ヒント (プレビュー)](../api-reference/beta/resources/mailtips.md) をチェックして、受信者に関する有用な情報を得る (受信者が自動返信を送信中なのか、あるいはメールボックスがいっぱいなのかなど)。</span><span class="sxs-lookup"><span data-stu-id="334bd-128">Check [mail tips (preview)](../api-reference/beta/resources/mailtips.md) while still composing a message to get useful status information about a recipient (such as the recipient sending an auto-reply or has a full mailbox).</span></span> <span data-ttu-id="334bd-129">メール ヒントは、アプリに対して特定の条件を警告することにより、フォローアップのアクションの効率を上げることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-129">Mail tips can alert apps of certain conditions so to take more efficient follow-up actions instead.</span></span> 

- <span data-ttu-id="334bd-130">[連絡先 API](people_example.md) の利用により、アプリの中で連絡先を選択するなど、対話式のコントロールが提供されます。</span><span class="sxs-lookup"><span data-stu-id="334bd-130">Make use of the [people API](people_example.md) to provide interactive controls such as a people picker in your app.</span></span> <span data-ttu-id="334bd-131">連絡先 API では、ユーザーの通信および共同作業のパターン、そしてビジネス上の付き合いに基づいて、ユーザーに最も関係の深い連絡先を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-131">The people API can suggest persons most relevant to a user, based on the user’s communication and collaboration patterns and business relationships.</span></span> 

- <span data-ttu-id="334bd-132">アプリ ユーザーに対して、メッセージ作成中に添付ファイルに関連して、気の利いたファイル選択機能を提供したり、最近利用したファイルを提案したりする。</span><span class="sxs-lookup"><span data-stu-id="334bd-132">Offer app users a smart file picker and suggest files that they have recently interacted with, to add as attachments when composing a message.</span></span> <span data-ttu-id="334bd-133">[Insights](../api-reference/beta/resources/insights.md) では、高度な分析機能を使用することにより、ユーザーの周辺で頻繁に使用されるファイル、最近ユーザーが表示または編集したファイル、あるいはそのユーザーと共有したファイルについての提案がなされます。</span><span class="sxs-lookup"><span data-stu-id="334bd-133">[Insights](../api-reference/beta/resources/insights.md) use advanced analytics to suggest files that are trending around a user, recently viewed or edited by the user, or shared with the user.</span></span>


### <a name="store-app-data-in-a-resource-or-resource-instance"></a><span data-ttu-id="334bd-134">アプリ データをリソースまたはリソース インスタンスに保存する</span><span class="sxs-lookup"><span data-stu-id="334bd-134">Store app data in a resource or resource instance</span></span>

<span data-ttu-id="334bd-135">アプリでは、データを外部データ ストアに保存するために、データの管理とアクセスのためのオーバーヘッドが発生することが少なくありません。</span><span class="sxs-lookup"><span data-stu-id="334bd-135">Often times apps have to store their data in an external data store and entail overhead in managing and accessing the data.</span></span> <span data-ttu-id="334bd-136">アプリで Microsoft Graph を使用すれば、単に[カスタム データを個々のリソース インスタンスに保存](extensibility_overview.md#open-extensions)するか、あるいは該当する場合には、スキーマを拡張し、カスタム プロパティを追加して、Microsoft Graph リソースの中に型指定されたデータを保存することができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-136">Microsoft Graph lets your app simply [store custom data in individual resource instances](extensibility_overview.md#open-extensions), or, if appropriate, extend the schema, add custom properties, and store typed data in Microsoft Graph resources.</span></span> <span data-ttu-id="334bd-137">そのような[スキーマ拡張](extensibility_overview.md#schema-extensions)を、検出可能また共有可能なものにすることができます。</span><span class="sxs-lookup"><span data-stu-id="334bd-137">You can make such [schema extensions](extensibility_overview.md#schema-extensions) discoverable and shareable.</span></span> 


## <a name="next-steps"></a><span data-ttu-id="334bd-138">次の手順</span><span class="sxs-lookup"><span data-stu-id="334bd-138">Next steps</span></span>

- <span data-ttu-id="334bd-139">[Graph Explorer](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages&version=v1.0) で Outlook メール サンプル クエリを選択して試行する。</span><span class="sxs-lookup"><span data-stu-id="334bd-139">Select and try Outlook mail sample queries in [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer/?request=me%2Fmessages&version=v1.0).</span></span> <span data-ttu-id="334bd-140">左側の列の **[サンプルをさらに表示]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="334bd-140">Choose **Show more samples** in the column on the left.</span></span> <span data-ttu-id="334bd-141">メニューを使用して **Outlook メール** をオンにします。</span><span class="sxs-lookup"><span data-stu-id="334bd-141">Use the menu to turn on **Outlook Mail**.</span></span>
- <span data-ttu-id="334bd-142">以下について調べます。</span><span class="sxs-lookup"><span data-stu-id="334bd-142">Learn about:</span></span>

  - [<span data-ttu-id="334bd-143">メッセージの作成と送信</span><span class="sxs-lookup"><span data-stu-id="334bd-143">Creating and sending messages</span></span>](outlook-create-send-messages.md)
  - <span data-ttu-id="334bd-144">[メッセージの整理方法](outlook-organize-messages.md)</span><span class="sxs-lookup"><span data-stu-id="334bd-144">Ways to [organize messages](outlook-organize-messages.md)</span></span>
  - <span data-ttu-id="334bd-145">[メッセージ フォルダーを共有する](outlook-share-messages-folders.md)方法</span><span class="sxs-lookup"><span data-stu-id="334bd-145">How to [share message folders](outlook-share-messages-folders.md)</span></span>

- <span data-ttu-id="334bd-146">Microsoft Graph v1.0 での[メール API の使用](../api-reference/v1.0/resources/mail_api_overview.md) とその[用途](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases)について調べる。</span><span class="sxs-lookup"><span data-stu-id="334bd-146">Find out more about [using the mail API](../api-reference/v1.0/resources/mail_api_overview.md) and its [use cases](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) in Microsoft Graph v1.0.</span></span>

