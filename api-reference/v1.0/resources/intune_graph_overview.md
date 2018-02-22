# <a name="working-with-intune-in-microsoft-graph"></a>Microsoft Graph での Intune の操作  

> **注:**Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://www.microsoft.com/ja-JP/cloud-platform/microsoft-intune-pricing)を持っている必要があります。

Intune 用 Microsoft Graph API を使用すると、テナントの Intune の情報へのプログラムによるアクセスが可能となります。API は **Azure Portal** で使用できるものと同じ Intune 操作を実行します。  

モバイル デバイス管理 (MDM) のシナリオの場合、Intune 用 Graph API はスタンドアロンの展開をサポートします。Intune の[ハイブリッド展開](https://docs.microsoft.com/ja-JP/sccm/mdm/understand/choose-between-standalone-intune-and-hybrid-mobile-device-management)はサポートされていません。 

## <a name="using-the-intune-graph-api"></a>Intune Graph API の使用

Intune は、豊富なエンティティ情報とリレーションシップのナビゲーションを使用して、他のクラウド サービスと同じ方法で Microsoft Graph API にデータを提供します。  Microsoft Graph API を使用して、他のサービスからの情報と Intune を結合し、IT プロフェッショナルやエンド ユーザー向けの豊富なサービス間アプリケーションをビルドします。     

以下に、アプリケーションがユーザーのデバイスにインストールされているかどうかを判断する方法の例を示します。 

1. Azure Active Directory から、ユーザーに登録されているデバイスのリストを取得します。 

    https://graph.microsoft.com/users/{user}/ownedDevices 

2. 次に、テナントのアプリケーションのリストを表示します。 

    https://graph.microsoft.com/deviceAppManagement/mobileApps  

3. アプリケーションから ID を取得し、アプリケーション (そしてユーザー) のインストール状態を確認します。

    https://graph.microsoft.com/deviceAppManagement/mobileApps/{id}/deviceStatuses/


## <a name="using-permission-scopes"></a>アクセス許可のスコープの使用

Microsoft Graph API では、アクセス許可のスコープによってリソースへのアクセスを制御します。 開発者は、Intune リソースにアクセスするために必要となる、アクセス許可のスコープを指定する必要があります。 通常は Azure Active Directory ポータルで必要なアクセス許可のスコープを指定します。 詳細については、「[Microsoft Graph のアクセス許可スコープ](https://developer.microsoft.com/ja-JP/graph/docs/authorization/permission_scopes)」および「[Intune のアクセス許可のスコープ](https://developer.microsoft.com/ja-JP/graph/docs/authorization/permission_scopes#permission-scopes-in-preview)」を参照してください。
