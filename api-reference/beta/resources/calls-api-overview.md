---
title: 呼び出しと Microsoft Graph のオンライン会議の API を使用します。
description: Microsoft Graph を呼び出すし、オンライン会議の API は、どのアプリやサービスがユーザーと対話する音声機能とビデオ機能を有効にして新しいディメンションを追加します。 API を使用すると、呼び出しを作成し、ユーザーとマイクロソフトのチームでのアプリケーションからの呼び出しを受信できます。 これらの Api を使用するには、通話や会議の参加者として機能するサービス アプリケーション (bot) を構築します。
ms.openlocfilehash: fcb1d69e204f5bba7c1ece01bcd61ae21f6ca6b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27066812"
---
# <a name="working-with-the-calls-and-online-meetings-api-in-microsoft-graph"></a>呼び出しと Microsoft Graph のオンライン会議の API を使用します。

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

Microsoft Graph を呼び出すし、オンライン会議の API は、どのアプリやサービスがユーザーと対話する音声機能とビデオ機能を有効にして新しいディメンションを追加します。 API を使用すると、呼び出しを作成し、ユーザーとマイクロソフトのチームでのアプリケーションからの呼び出しを受信できます。 これらの Api を使用するには、通話や会議の参加者として機能するサービス アプリケーション (bot) を構築します。

## <a name="call-types"></a>呼び出しの種類

呼び出しは、ピア ツー ピアまたはマルチパーティの通話として分類されます。 ユーザーでは、ボット、ピア ツー ピアの呼び出しを開始したり、bot を既存のマルチパーティの会議に招待することができます。 アクセス許可は必要ありません、ユーザーがピア ツー ピアの呼び出しに bot を招待するときです。 Bot マルチパーティの通話に参加するには、bot をグループに参加するのにはテナント管理者のアクセス許可を持つ必要があります。

![ピア ツー ピアとマルチパーティの呼び出しが表示された画像](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/call-types.png)

Bot が呼び出しを作成する場合、開始または初期化の呼び出しグループのアクセス許可のいずれかを持つ必要があります。 ボットには、ピア ツー ピアの呼び出しまたは複数の呼び出しを作成するオプションがあります。

- ピア ツー ピアの呼び出しでは、bot が 1 つだけの対象としない会議座標を指定する必要があります。 
- ボットは、複数の参加者との呼び出しを開始した場合、暫定的な会議がバック グラウンドで設定されていると、その会議に参加するすべてのユーザーです。 会議の座標を指定すると、ターゲットを 1 つだけがある場合でもに、マルチパーティの呼び出しを設定します。

呼び出しは、ピア ツー ピアとして開始し、マルチパーティにエスカレートする可能性があります。 会議が自動的にプロビジョニングし、メディアは、会議を再度作成します。 ボットは、ボットは、呼び出しの開始のグループ アクセス許可を持っていれば、他の人を招待してエスカレーションを開始できます。 他の参加者によってエスカレーションが開始され、bot が呼び出しの結合のグループのアクセス許可を持たない、bot の呼び出しから削除されます。

> **重要な:** マルチパーティには、ピア ツー ピアからの呼び出しがエスカレート、ときに複数のすべての機能を利用できます。 具体的には、bot には、名簿の更新プログラムは表示されません。

## <a name="signaling"></a>シグナル

### <a name="incoming-call"></a>着信呼び出し

着信呼び出しを受信するには、呼び出し側の bot を登録する必要があります。 Bot は、着信の通知を受信するときは、次のオプションがあります。

| メソッド                              | 説明                                  |
|:------------------------------------|:---------------------------------------------|
| [回答](../api/call-answer.md)     | 着信呼び出しに応答します。                    |
| [Reject](../api/call-reject.md)     | 却下して呼び出しを切断します。                  |
| [リダイレクト](../api/call-redirect.md) | 呼び出しをリダイレクトします。                           |

Bot は、他のユーザーまたは bot への呼び出しをリダイレクトできます。 Bot によっては、ユーザーのボイス メールにリダイレクトすることができます。

![Bot のボイス メールの呼び出しをリダイレクトすることを示す画像](https://cdn.graph.office.net/prod/GraphDocuments/en-us/concepts/images/call-handling.png)

> **重要な:** リダイレクトしたり、PSTN への発信コールをすることは現在サポートされていません。

### <a name="in-call"></a>呼び出しで

Bot 用の操作は、呼び出しオブジェクトで使用できます。 Bot は、呼び出しの参加者としてこれらに影響します。

| メソッド                                                            | 説明                                  |
|:------------------------------------------------------------------|:---------------------------------------------|
| [ミュート](../api/call-mute.md)                                       | 呼び出しで自身をミュートします。                       |
| [ミュート解除します。](../api/call-unmute.md)                                   | 呼び出しで自身のミュートを解除します。                     |
| [UpdateMetadata](../api/call-updatemetadata.md)                   | 名簿に、自身のメタデータを更新します。          |
| [ChangeScreenSharingRole](../api/call-changescreensharingrole.md) | 起動し、画面の呼び出しでの共有を停止します。   |

呼び出しでは、他の参加者との対話をするには、参加者のオブジェクトを使用します。

| メソッド                                                            | 説明                                  |
|:------------------------------------------------------------------|:---------------------------------------------|
| [参加者の一覧](../api/call-list-participants.md)             | 構成要素オブジェクトのコレクションを取得します。         |
| [参加者を招待します。](../api/participant-invite.md)               | アクティブな通話に参加者を招待します。      |
| [参加者全員をミュートします。](../api/participant-muteall.md)            | 呼び出しのすべての参加者をミュートします。           |

## <a name="media"></a>メディア

メディア処理は、マイクロソフトのリアルタイム メディアのプラットフォームを介して管理されます。 リアルタイム メディアのプラットフォームでは、マイクロソフトのチームのオーディオとビデオ通話や会議に参加するボットことができます。 ピア ツー ピアとマルチパーティの両方の呼び出しに参加するためのリアルタイムの bot ことができます。

Bot は、着信呼に応答か、新規または既存の呼び出しを結合、リアルタイム メディアのプラットフォームにメディアの処理方法を確認する必要があります。 対話型音声応答 (IVR) システムを構築する場合は、高価なオーディオ コンポーネントの Microsoft のサービスがホストされているメディアを処理をオフロードできます。 ボットは、メディア ストリームへの直接アクセスを必要とする場合は、リアルタイム メディア SDK からのメディアのアプリケーションでホストされているオプションを提供しています。

### <a name="service-hosted-media"></a>メディアのサービスでホストされています。

Bot では、ワークフローを管理でき、マイクロソフトのリアルタイム メディアのプラットフォームへのオーディオの処理の負荷を軽減することができます。 サービスでホストされているメディアを実装して、ボットをホストするためにいくつかのオプションがあります。 利用可能な[Sdk](https://developer.microsoft.com/graph/code-samples-and-sdks)のいずれかを使用してください。 メディアのサービスでホストされているボットは、メディアをローカルに処理されないと、ステートレスなサービスとして実装できます。

| メソッド                                                        | 説明                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------|
| [PlayPrompt](../api/call-playprompt.md)                       | ユーザーにオーディオ クリップを再生します。                         |
| [Record](../api/call-record.md)                               | 必要に応じてメッセージを再生し、オーディオ クリップを録音します。      |
| [SubscribeToTone](../api/call-subscribetotone.md)             | ユーザーの DTMF トーンを購読します。                  |
| [CancelMediaProcessing](../api/call-cancelmediaprocessing.md) | 処理キューに入っている既にメディアをキャンセルします。             |

### <a name="application-hosted-media"></a>アプリケーションによってホストされるメディア

メディアへの直接アクセスを取得する bot、bot では、メディアのアクセス許可を必要があります。 リアルタイム メディア ライブラリおよびステートフルな SDK をボットを呼び出すリアルタイム リッチ ・ メディアを作成できます。 Windows 環境で、アプリケーションによってホストされるボットをホストする必要があります。 [メディア サンプルがアプリケーションにホストされている](https://github.com/microsoftgraph/microsoft-graph-comms-samples)クラウド サービスとサービス ・ ファブリックなど、さまざまな Azure プラットフォームでボットを構築する方法を表示します。

[Microsoft グラフの呼び出しの SDK](https://microsoftgraph.github.io/microsoft-graph-comms-samples/docs/articles/index.html)を使用すると、bot の作成を簡略化します。 SDK には、メモリ内のリソースの状態を管理して、bot 開発者のメディアのスタックを取得する機能が用意されています。

Media SDK は、コンテンツの送信および受信のオーディオ、ビデオ、およびビデオ ・ ベースの画面を共有する bot を使用できます。 ビデオ ベースの画面の共有は、ビデオのチャンネルとしてモデル化されます。 Bot は、オーディオ チャンネルを混合し、複数のビデオ チャンネルを購読できます。 ビデオのチャンネルでは、bot が送受信するようにビデオを H.264 エンコード済みストリーム、またはデコードされた生のフレームとして選択します。

> **注:** 記録またはそれ以外の場合の呼び出しや、ボットにアクセスするための会議からのメディアの内容を保持する Microsoft.Graph.Calls.Media API を使用することがあります。

## <a name="see-also"></a>関連項目

[通話やオンライン会議の API のサンプル](https://github.com/microsoftgraph/microsoft-graph-comms-samples/)

[既知の問題](/graph/known-issues#calls-and-online-meetings)