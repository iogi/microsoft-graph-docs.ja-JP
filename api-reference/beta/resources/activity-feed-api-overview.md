---
title: アクティビティ フィードの REST API を使用します。
description: 'Graph API のフィード アクティビティを使用するにはデバイスやプラットフォーム間でユーザーのアクティビティを再開します。 アクティビティ フィードの API 要求は、委任されたアクセス許可とユーザーのアクティビティ権限、個人または仕事や学校のアカウントで使用できるユーザーの代わりに実行されます。 '
ms.openlocfilehash: 8f66f7b991df361c96404d4fe1a3c9d19faf2436
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27066810"
---
# <a name="use-the-activity-feed-rest-api"></a>アクティビティ フィードの REST API を使用します。

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。


Graph API のフィード アクティビティを使用するにはデバイスやプラットフォーム間でユーザーのアクティビティを再開します。 アクティビティ フィードの API 要求は、[委任されたアクセス許可](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions)と[ユーザーの活動のアクセス権](/graph/permissions-reference)、個人または仕事や学校のアカウントを使用できるユーザーの代わりに実行されます。 

ユーザー アクティビティが[アクティビティ](https://developer.microsoft.com/graph/docs/api-reference/beta/resources/projectrome_activity)のリソースによって表されで構成されて、時間ベースのフィードで表されるコレクション私と活動します。 
<!-- Add missing content.
Each activity represents a unique... 
-->
## <a name="what-makes-a-great-user-activity"></a>優れたユーザー アクティビティの特長は、

ユーザー ・ アクティビティがないアプリケーションを起動して、-アプリ内の特定のコンテンツを高度なリンクであります。 作成するユーザーのアクティビティは、独自のアプリケーションでしか使用できませんが、Cortana および Windows のタイムラインにも表示されます、アプリケーションの複数の reengagement を推進し、複数のデバイス間でのアプリの使用を続行する、ユーザーに容易にします。  

### <a name="what-should-become-an-activity"></a>活動になりますどのような必要がありますか。 

すべてのアプリケーションが異なるため、各アプリケーション開発者がユーザーの利用状況、アプリケーション内で操作をマップする最善の方法を理解するです。 などのゲームは、各キャンペーンの活動を作成可能性があります、文書作成アプリケーションはそれぞれ固有のドキュメントのアクティビティを作成可能性があり、基幹業務アプリケーションは、各ワークフローのアクティビティを作成可能性があります。 

アプリで activitites を定義する際は、次のガイドラインを適用します。

**の操作を行います:** 関連するユーザー ・ アクションのグループの 1 つのアクティビティを記録します。 関連コンテンツの一連のアプリケーションを使用する場合おそらく理にかなって契約全体のセッションの 1 つのアクティビティを記録します。  

*再生リストのシナリオ:* これは、特に、音楽の再生リストやテレビ番組の関連: 進捗状況を表示するのには 1 人のユーザーのアクティビティを更新することができます。 この例では、単一のユーザーのアクティビティを複数の[履歴項目](https://developer.microsoft.com/graph/docs/api-reference/beta/resources/projectrome_historyitem)が複数の数日または数週間にわたって活動の期間を表すがあります。  

**の操作を行います:** クラウドに移行するユーザー データを格納します。 デバイス間の活動をサポートする場合は、クラウド ストレージの場所にこのアクティビティを reengage に必要なコンテンツが格納されているかどうかを確認する必要があります。 などのアクティビティをユーザーがドキュメントを編集するたびに発行する場合、ドキュメントする必要があるクラウドに格納はなくユーザーのデバイス上でローカルにデバイス間の reengagement を有効にするために。  

**しない:** 操作をユーザーが後で再開する必要はありませんのユーザーのアクティビティを作成します。 将来的に追跡するための状態は保持されません、シンプルな 1 回限りの操作を実行するアプリケーションを使用する場合、おそらくはユーザーの活動を作成する必要はありません。 

明確にするため、Windows のタイムラインでのユーザーのアクティビティが表示される場合でもこのとして設計されていないバージョン管理ツール、ドキュメント ベースのアクティビティを選択することは、(他のユーザーによって加えられた変更を含む)、そのドキュメントの最新バージョンを常に表示する必要があります

**しない:***他のユーザー*によって完了したアクションのユーザーのアクティビティを作成します。 ユーザーが送信されるは、メッセージ、またはアプリケーション内でユーザーを @mentions、新しい活動を書き込む必要がありますされません。 これらの相互作用方が通知を提示します。  

*コラボレーションのシナリオ:* 複数のユーザーは、同じアクティビティ (Word ドキュメントなど) で作業している場合、場合もあります別のユーザーが変更を行った文書を最後に編集した後にします。 この例では、アプリの開発者は、ドキュメントに対する変更を反映するようにアクティビティの視覚的な要素を更新する場合があります。 これを行うには、アプリケーションは、新しい履歴項目を作成することがなく既存のアクティビティを更新することがあります。 

>**注:** 両方を含めるには web アプリケーションの活動を公開する場合、`activationURL`と`fallbackURL`の活動のそれぞれのです。 活動が Windows のタイムラインのように、マイクロソフトの経験から期待どおりには、アプリにユーザーを起動します。 

## <a name="app-interaction-patterns-and-user-activities"></a>アプリケーションとの対話のパターンとユーザーの活動 
ユーザー ・ アクティビティを作成するには、アプリケーションの相互作用のパターンによって異なります。 すべてのアプリケーションは異なるが、ほとんどは、対話のパターンを次のいずれかに分類されます。 

* **ドキュメント ベースのアプリケーション**ドキュメントあたり 1 つのアクティビティの使用の期間を反映した 1 つまたは複数の履歴レコードを作成します。 ドキュメントに変更を加えると、活動カードを更新するために重要です。 
* **メディア再生アプリ**再生リスト、プログラム、またはスタンドアロンのコンテンツなどのコンテンツの論理的なグループごとに 1 つのアクティビティを作成します。 
* **ゲーム**またはゲームの世界は、保存ごとに 1 つのアクティビティを作成します。 ゲームでは、レベルの 1 つのシーケンスのみがサポートされている場合、最新の進行状況や達成状況を表示するのには、カードを更新することもできますが、時間の経過とともに同じアクティビティを記述できます。 
* **ユーティリティ アプリケーション**-活動を公開するユーザーが再開する必要があるアプリケーション内で何がある場合は、しない必要があります。 良い例は、電卓のような簡単な専用アプリケーションです。 
* **基幹業務アプリケーション**などの単純なタスクまたはワークフローを管理するのには多くのアプリケーションが存在します。 独立したワークフローは、アプリを使用してアクセスごとに 1 つのアクティビティを作成します。 などの各経費精算書になります別のアクティビティでは、その活動をすることが承認されたかどうかを参照してください] をクリックすることができますので。

*いくつかの複雑なアプリケーションには、複数の相互作用のパターンが含まれています。さまざまなシナリオが、アプリケーションによって処理される別のユーザー アクティビティの作成パターンに従うこともできます。*

<!-- Add content or remove H2.
## Common use cases 
-->

## <a name="next-steps"></a>次の手順

- [アクティビティのリソース](https://developer.microsoft.com/graph/docs/api-reference/beta/resources/projectrome_activity)を参照してくださいし、の重要なタスクを再開するユーザーを支援するアプリのアクティビティを定義します。
- 活動**pop**にするアイデアの[アダプティブ ・ カードのサンプル](https://adaptivecards.io/samples/)のサンプルを表示します。  
- [Graph エクスプローラー](https://developer.microsoft.com/graph/graph-explorer)で API をお試しください。

**詳細については調べていますか。** 

- [アクティビティを使用しているマイクロソフトの経験](https://channel9.msdn.com/events/Build/2017/B8108)を参照してください。
- [アクティビティ フィードの API と中断した場所を選択](https://channel9.msdn.com/Events/Windows/Windows-Developer-Day-Fall-Creators-Update/WinDev011)について説明します。