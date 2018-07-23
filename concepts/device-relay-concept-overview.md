# <a name="device-relay-api-in-microsoft-graph-preview"></a><span data-ttu-id="7774b-101">Microsoft Graph のデバイス リレー API (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="7774b-101">Device relay API in Microsoft Graph (preview)</span></span>

<span data-ttu-id="7774b-102">今日のユーザーは日常的に複数のデバイスを操作しています。</span><span class="sxs-lookup"><span data-stu-id="7774b-102">Today, people interact with multiple devices on a daily basis.</span></span> <span data-ttu-id="7774b-103">多くの場合、ユーザーは生産性タスクとエンターテイメント活動をあるデバイスで開始し、別のデバイスで継続します。</span><span class="sxs-lookup"><span data-stu-id="7774b-103">Users often start productivity tasks and entertainment activities on one device and continue them on another.</span></span> <span data-ttu-id="7774b-104">顧客のニーズを満たすには、複数のデバイスやプラットフォームにまたがってアプリをシームレスに使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7774b-104">To meet your customers' needs, your apps need to seamlessly span devices and platforms.</span></span> 

<span data-ttu-id="7774b-105">デバイス リレー API を使用すると、ユーザーにシームレスなエクスペリエンスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="7774b-105">You can use the device relay APIs to deliver seamless experiences to your users.</span></span> <span data-ttu-id="7774b-106">ユーザーは、あるデバイスから別のデバイスにエクスペリエンスをアクティブに転送したり、同時に複数のデバイスを使用してエクスペリエンスを強化したりできます。</span><span class="sxs-lookup"><span data-stu-id="7774b-106">You can make it possible for them to actively transfer an experience from one device to another or enhance it by using multiple devices at once.</span></span> <span data-ttu-id="7774b-107">これは、アプリ内のアクション (アプリ内のボタンや選択) によってデバイス リレー API を呼び出すことで行われます。呼び出された API は、ユーザーのデバイスを検出したり、デバイスで他のデバイスのアプリを起動してメッセージを送信したりします。</span><span class="sxs-lookup"><span data-stu-id="7774b-107">This is done via in-app actions (a button or selection in your app) that call the device relay API to discover users' devices, and enable them to launch and message your app on those other devices.</span></span>

## <a name="why-integrate-with-device-relay"></a><span data-ttu-id="7774b-108">デバイス リレーと統合する理由</span><span class="sxs-lookup"><span data-stu-id="7774b-108">Why integrate with device relay?</span></span>

<span data-ttu-id="7774b-109">デバイス リレー API は、アプリがユーザーのデバイス上でアプリの登録、検出、指示、およびメッセージ送信を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7774b-109">The device relay API enables your app to register itself, and discover, command, and message your app on the user's devices.</span></span> <span data-ttu-id="7774b-110">このようにすることで、顧客が作業するタスクを中心に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="7774b-110">By doing this, you can make the tasks your customers work on the central focus.</span></span> <span data-ttu-id="7774b-111">デバイスを検出し、そこにタスクを転送することで、ユーザーは自分にとって最も便利なデバイスで作業できます。</span><span class="sxs-lookup"><span data-stu-id="7774b-111">They can work on the device that is most convenient for them by discovering it and transferring tasks to it.</span></span> <span data-ttu-id="7774b-112">また、アプリで継続中のエクスペリエンスを、周囲の他のデバイスを使用して強化することもできます。</span><span class="sxs-lookup"><span data-stu-id="7774b-112">They can also enhance an ongoing experience with your app by using other devices around them.</span></span>

<span data-ttu-id="7774b-113">デバイス リレー API は、コンパニオン デバイスまたはリモート制御のシナリオで使用できます。</span><span class="sxs-lookup"><span data-stu-id="7774b-113">You can use the device relay API for companion devices, or remote control scenarios.</span></span> <span data-ttu-id="7774b-114">メッセージング機能を使用して、2 台のデバイス間にカスタム メッセージを送受信するためのアプリ チャネルを作成します。</span><span class="sxs-lookup"><span data-stu-id="7774b-114">Use the messaging capabilities to create an app channel between two devices to send and receive custom messages.</span></span> <span data-ttu-id="7774b-115">たとえば、顧客が自分の電話を使用してテレビのプレイバックを制御できるようになります。</span><span class="sxs-lookup"><span data-stu-id="7774b-115">For example, you can enable your customers to use their phone to control playback on a TV.</span></span> <span data-ttu-id="7774b-116">また、生産性のシナリオで、ユーザーが PC 上のアプリのメインビューで作業している間に、電話でよく使用されるコンテキストベースのアクションを表示するコンパニオン アプリを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="7774b-116">You could also provide a companion app in a productivity scenario by displaying context-based commonly used actions on a phone while your users work on the main view of your app in the PC.</span></span>

<span data-ttu-id="7774b-117">顧客は、アプリ内のアクションを実行することで、あるデバイスから別のデバイスにエクスペリエンスをアクティブに転送することもできます。</span><span class="sxs-lookup"><span data-stu-id="7774b-117">Your customers can also actively transfer an experience from one device to another by performing an action in your app.</span></span> <span data-ttu-id="7774b-118">たとえば、バスの乗車中に自分の電話でライブ ブロードキャストを視聴しているユーザーは、自宅に着いたときに居間の PC にプレイバックを転送したいと思うかもしれません。</span><span class="sxs-lookup"><span data-stu-id="7774b-118">For example, a user might be watching a live broadcast on her phone while on the bus, but when she gets home she wants to transfer playback to the PC in her living room.</span></span> <span data-ttu-id="7774b-119">デバイス リレーでは、生産性のシナリオもサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7774b-119">Productivity scenarios are also supported by device relay.</span></span> 

### <a name="extend-the-experience"></a><span data-ttu-id="7774b-120">エクスペリエンスの拡張</span><span class="sxs-lookup"><span data-stu-id="7774b-120">Extend the experience</span></span>

<span data-ttu-id="7774b-121">デバイスを検出し、それらのデバイスでアプリを起動する UX を提供することで、アプリを拡張します。</span><span class="sxs-lookup"><span data-stu-id="7774b-121">Extend your app by providing UX to discover devices and to launch your app on those devices.</span></span> <span data-ttu-id="7774b-122">たとえば、ユーザーは自分の電話で発注書の作業を行い、自分のオフィスの PC を検出し、その PC のアプリを起動して発注書の入力を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="7774b-122">For example, the user could be working on a purchase order on her phone, discover the PC in her office, and launch the app there to finish entering the purchase order.</span></span>  

### <a name="augment-the-experience"></a><span data-ttu-id="7774b-123">エクスペリエンスの補強</span><span class="sxs-lookup"><span data-stu-id="7774b-123">Augment the experience</span></span>

<span data-ttu-id="7774b-124">ユーザーの別のデバイス上のアプリ用のコンパニオン エクスペリエンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="7774b-124">Create a companion experience for your app on another of the user’s devices.</span></span> <span data-ttu-id="7774b-125">たとえば、アプリに他のデバイス上でそのアプリを起動する UX を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7774b-125">For example, the app could include UX to launch itself on other devices.</span></span> <span data-ttu-id="7774b-126">ゲームでは、ユーザーが大画面を備えたデバイスに (たとえば、PC から Xbox に) アプリを移動して起動できます。</span><span class="sxs-lookup"><span data-stu-id="7774b-126">In a game, the user could launch the app to a device with a larger screen (for example, from a PC to an Xbox).</span></span> <span data-ttu-id="7774b-127">Xbox でゲームの完全なビュー (一人称ビュー) を表示しながら、画面の小さいデバイスでコンテキストを追加した異なるビュー (プレーヤーと対戦相手の場所を示すゲームの最上位ビュー) を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7774b-127">The Xbox could present a full view of the game (a first-person view), while the device with the smaller screen could present a different view with additional context (a top-level view of the game level showing the player and opponents' locations).</span></span>  

### <a name="enrich-the-experience"></a><span data-ttu-id="7774b-128">エクスペリエンスの強化</span><span class="sxs-lookup"><span data-stu-id="7774b-128">Enrich the experience</span></span>

<span data-ttu-id="7774b-129">制御機能をアプリに追加します。</span><span class="sxs-lookup"><span data-stu-id="7774b-129">Add additional controlling abilities to your app.</span></span> <span data-ttu-id="7774b-130">たとえば、コンパニオン デバイスからメイン アプリのリモート制御機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="7774b-130">For example, provide remote control abilities for the main app from a companion device.</span></span> <span data-ttu-id="7774b-131">ユーザーがあるデバイスから別のデバイスのアプリを起動したときに、ソース デバイスでターゲット デバイスのアプリの状態に応じて最もよく使用されるアクションのリスト (たとえば、回転、サイズ変更、カラー パレットなど) を表示しながら、ターゲット デバイスで完全なエクスペリエンス (たとえば、デザイン アプリの 3D モデルなど) を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7774b-131">When the user launches an app from one device to another, the target device could show the full experience (for example, a 3D model in a design app), while the source device could show a list of the most common actions given the state of the app on the target device (for example, rotate, resize, color palette).</span></span>

## <a name="see-also"></a><span data-ttu-id="7774b-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="7774b-132">See also</span></span>

- [<span data-ttu-id="7774b-133">Microsoft Graph のクロスデバイス エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="7774b-133">Cross-device experiences in Microsoft Graph</span></span>](cross-device-concept-overview.md)
- [<span data-ttu-id="7774b-134">デバイス リレー API に関する詳細情報</span><span class="sxs-lookup"><span data-stu-id="7774b-134">Learn more about the device relay API</span></span>](../api-reference/beta/resources/project_rome_overview.md)
- [<span data-ttu-id="7774b-135">Project Rome に関する詳細情報</span><span class="sxs-lookup"><span data-stu-id="7774b-135">Learn more about Project Rome</span></span>](http://aka.ms/projectrome)