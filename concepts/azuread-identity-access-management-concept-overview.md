---
title: Azure AD ID およびアクセス管理 API の概要
description: 'Azure Active Directory (Azure AD) は、ID およびアクセス管理 (IAM) を集中管理し、アプリ、デバイス、サービス、およびインフラストラクチャの間でのセキュアで生産性の高いアクセスを可能にします。 組織では、Azure AD を使用することにより、オンプレミス、ハイブリッド、およびクラウドの各環境において、ID およびコントロール アクセスを管理することができます。  '
ms.openlocfilehash: f933e47f890f228865968d47040fdb1316607692
ms.sourcegitcommit: 4a46cfd112c8089fc07e4e5ccdccaf415a3a0e7f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2018
ms.locfileid: "27156048"
---
# <a name="azure-ad-identity-and-access-management-api-overview"></a>Azure AD ID およびアクセス管理 API の概要

Azure Active Directory (Azure AD) は、ID およびアクセス管理 (IAM) を集中管理し、アプリ、デバイス、サービス、およびインフラストラクチャの間でのセキュアで生産性の高いアクセスを可能にします。 組織では、Azure AD を使用することにより、オンプレミス、ハイブリッド、およびクラウドの各環境において、ID およびコントロール アクセスを管理することができます。  

Microsoft Graph で Azure AD REST API を使用することにより、Azure AD の[リソース](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0)とサード パーティ サービスの間での固有ワークフローを作成することができます。

## <a name="why-use-the-azure-ad-apis"></a>Azure AD API を使用する理由

1500 万を超える組織で Azure AD が使用されており、さらに、Office 365、Microsoft Azure、Enterprise Mobility Suite、または Microsoft 365 などの Microsoft クラウド サービスのサブスクリプションを取得しています。  

企業開発者は、Microsoft Graph を使用することにより、Azure AD ID 管理と他のサービスを統合して、従業員研修 (および終了)、プロファイル管理、ライセンス展開などの管理ワークフローを自動化します。

多くの企業開発者にとって Microsoft Graph および Azure AD は、既存のアプリケーションをクラウドに「リフトおよびシフト」して、組織のデジタル変換のスピードを上げるのに役立ちます。 Azure AD のさまざまな機能を利用することにより、ユーザーのグループ メンバーシップ、ディレクトリの役割、または管理単位メンバーシップの確認など、アクセス制御メカニズムをアプリケーションに追加できます。

Microsoft Graph および Azure AD を、Azure AD サービスをすでに使用している Fortune 500 企業の 90% を含む 1500 万を超える組織にすばやく容易に達する手段として使用できます。 統合アプリケーションでは、シームレスなサインイン エクスペリエンスを利用することができ、既存の組織データを使用してカスタマイズしたエクスペリエンスを作成することができます。  

Microsoft Graph で Azure AD API を使用することにより、ユーザーのプロファイルについてのクエリの実行、他のユーザーの検索、組織の関係の管理、課題の追跡、既存の組織データを取り入れたオリジナル ソリューションの作成が可能です。 これらの API は、複数のカスタム ビジネス アプリケーションを、組織の既存のデジタル サービスにシームレスに統合するための強固な基盤を提供します。

### <a name="access-users-and-groups"></a>ユーザーおよびグループにアクセスする

Microsoft Graph で Azure AD API を使用することにより、次のことを実行できます:

- 組織内のユーザーの名前、写真、電子メール アドレス、役職、勤務先所在地やその他の[ユーザー プロファイル](/graph/api/resources/user?view=graph-rest-1.0)情報を検索し、管理する。
- 組織内のプロジェクトおよびチームの[グループ](/graph/api/resources/groups-overview?view=graph-rest-1.0)を作成する。 グループからメンバーを追加および削除し、リソースへのアクセスを制御する。 (動的グループでは、ユーザー プロパティの値に基づいてメンバーシップを自動的に変更することができます。)
- アクセスを制御するには、グループのリストで[推移メンバーシップ](/graph/api/user-checkmembergroups?view=graph-rest-1.0)をチェックしたり、[汎用リソース ID](/graph/api/directoryobject-getbyids?view=graph-rest-1.0) のリストから指定したタイプ (ユーザーやグループなど) のリソースすべてを取得したりすることができます。

### <a name="manage-directory-roles"></a>ディレクトリ ロールを管理する

事前定義済みの Azure AD 管理[ディレクトリ ロール](/graph/api/resources/directoryrole?view=graph-rest-1.0)にユーザーを割り当てることができます。これにより、特定のタスクを実行するための許可を付与できます。

### <a name="manage-devices"></a>デバイスを管理する

組織に登録されている[デバイスを管理](https://docs.microsoft.com/en-us/azure/active-directory/device-management-introduction)します。 デバイスはユーザーに登録されており、ノート PC、デスクトップ、タブレット、携帯電話などのアイテムを含みます。 デバイスは通常、Device Registration Service を使用するか、Microsoft Intune によって、クラウドで作成されます。 これは、多要素認証の条件付きアクセス ポリシーで使用されます。

### <a name="partner-tenant-management"></a>パートナー テナント管理

Microsoft オンライン サービス (Office 365、Microsoft Azure、CRM オンラインなど) を再販し、管理する Microsoft パートナーは、現在管理している[組織テナント](/graph/api/resources/contract?view=graph-rest-1.0)を表示できます。

テナントに関連付けられている[ドメインを管理](/graph/api/resources/domain?view=graph-rest-1.0)することもできます。 ドメイン操作によって Microsoft パートナーは、Office 365 などのサービスのドメインの登録を自動化することができます。

### <a name="tenant-management"></a>テナント管理

テナント管理用 Azure AD API により、次のことを実行できます:

- 会社住所、技術部連絡先、通知連絡先、アクティブなサービス サブスクリプション、それに関連付けられているドメインなど、[組織](/graph/api/resources/organization?view=graph-rest-1.0)に関する情報を取得します。
- 会社のサブスクライブ先の[サービス SKU](/graph/api/resources/subscribedsku?view=graph-rest-1.0) に関する情報を取得します。
- 組織に[外部 (ゲスト) ユーザーを招待](/graph/api/resources/invitation?view=graph-rest-1.0)します。

### <a name="monitor-identity-risks-preview"></a>リスクを識別する (プレビュー) を監視します。

ほとんどのセキュリティ侵害は、攻撃者がユーザーの ID を盗んだ結果としてなされており、第三者による侵害、パスワード スプレー攻撃、および高度なフィッシング攻撃を利用することで、ますます威力が増してきています。 したがって、ユーザー アカウントのすべてをそのような攻撃から保護し、無防備な ID が悪用されるのを事前に防ぐ必要があります。

Azure AD では、アカウントが無防備である可能性を示す異常を検出するために、アダプティブ機械学習アルゴリズムや経験則を使用します。 Azure AD の識別情報の保護はこのデータを使用すると、条件付きアクセスのリスク ・ ベースのポリシーを使用してユーザーを保護し、レポートとその検出の警告が生成されます。

今日では、Microsoft Graph により簡単にアクセスをなどの[クエリのリスク イベント Id 保護によって検出された](/graph/api/resources/identityprotection-root?view=graph-rest-beta)リスク イベントの種類、重要度、日付、時刻、場所、影響を受けるユーザーは、および複数に Azure AD プレミアム P2 の顧客にします。 お客様は、SIEM システムとセキュリティのアプリケーションでこれらのイベントを使用できます。

### <a name="activate-users-into-privileged-roles-preview"></a>特権ロール (プレビュー) にユーザーをアクティブにする

管理者権限をオンデマンドでアクティブ化することによってリソースへのアクセスをセキュリティで保護できます。 [特権 ID 管理](/graph/api/resources/privilegedidentitymanagement-root?view=graph-rest-beta)の機能は Azure AD Premium P2 で利用できます。

### <a name="manage-user-access-reviews-preview"></a>ユーザー アクセスの確認 (プレビュー) を管理します。

グループのメンバーシップ、およびアプリケーションへのアクセスのアクセス確認を構成できます。 [Access](/graph/api/resources/accessreviews-root?view=graph-rest-beta)は、Azure AD プレミアム P2 に示されています。

## <a name="api-reference"></a>API リファレンス

このサービスの API リファレンスを検索してください。

- [Azure AD id およびアクセス管理 API Graph v1.0](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0)
- [Azure AD id およびアクセス管理 API ベータ版の Microsoft Graph](/graph/api/resources/azure-ad-overview?view=graph-rest-beta)

## <a name="next-steps"></a>次の手順

- [Azure AD REST API の使用](/graph/api/resources/azure-ad-overview?view=graph-rest-1.0)方法を確認する。
- Azure AD を使用して Microsoft Graph の[認証](auth-overview.md)を実行する。
- [Azure AD サインイン](https://azure.microsoft.com/en-us/develop/identity/signin/)をアプリまたは Web サイトに統合する
- Azure AD API の最新情報については、[Changelog](changelog.md) を参照してください。
- Microsoft Graph の使用方法についてのさらに多くのアイデアについては、[サンプル](https://developer.microsoft.com/graph/graph/examples)を参照してください。