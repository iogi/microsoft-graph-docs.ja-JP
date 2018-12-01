---
title: Outlook メールの REST API を使用します。
description: Graph では、個人または組織のアカウントのユーザーの Outlook のメール データへのアクセスの認証を取得するアプリを使用できます。
ms.openlocfilehash: c17ecfb9cc4f2ac313ef176ff7f21d276e75cc37
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27022259"
---
# <a name="use-the-outlook-mail-rest-api"></a>Outlook メールの REST API を使用します。

Microsoft Graph では、個人または組織のアカウントにあるユーザーの Outlook メール データに、アプリからアクセスすることを許可できます。[適切な代理アクセス許可またはアプリケーション アクセス許可](/graph/permissions-reference)を使用すると、アプリはサインインしているユーザーまたはテナント内のユーザーのメール データにアクセスできます。メール データは、Office 365 の一部として Exchange Online 上のクラウド内に存在することも、[ハイブリッド展開](/graph/hybrid-rest-support)の Exchange On-Premise 上に存在することもあります。

## <a name="using-the-mail-rest-api"></a>メール REST API の使用

メール API 要求は、ユーザーの **id** プロパティ (一意の GUID)、電子メール アドレス、サインインしているユーザーの `me` ショートカット エイリアスで識別できる[ユーザー](../resources/user.md)に代わって実行されます。

電子メール メッセージは、[message](../resources/message.md) リソースによって表され、[mailFolder](../resources/mailfolder.md) で構成されています。メッセージとメール フォルダーは、`GET` 操作から取得できる **id** プロパティによって識別されます。

>**注:** 一般的に、メールボックス内で **message** と **mailfolder** ID が一意で不変であるとは想定しないでください。これは、コピー、移動、送信などの特定の操作の後に変更される可能性があります。

メッセージ本文は、HTML 形式またはテキスト形式にできます。

次のように、既知のフォルダー名を使用することができます`Inbox`、 `Drafts`、 `SentItems`、または`DeletedItems`のすべてのユーザーの既定では存在している特定のメール フォルダーを識別します。 サポートされている既知のフォルダー名の一覧については、「[mailFolder リソースの種類](../resources/mailfolder.md)」を参照してください。

たとえば、最初にフォルダー ID を取得せず、サインインしているユーザーの Outlook**送信済みアイテム**フォルダーにメッセージを取得できます。

```http
GET /me/mailFolders('SentItems')/messages?$select=sender,subject
```

## <a name="common-use-cases"></a>一般的なユース ケース

**message** リソースは、UI で利用可能な機能に対応する **categories**、**conversationId**、**flag**、**importance** などのプロパティを公開し、アプリを自動化したり、組み込みの Outlook ユーザー エクスペリエンスを統合したりできるようにします。

Microsoft Graph API には、メッセージの一般的なユース ケースをサポートするメソッドとアクションも用意されています。

| ユース ケース | REST リソース | 関連項目 |
|:----------|:---------------|:---------|
| **ユーザー指向のアクション** | | |
| メッセージを下書き、読み取り、返信、転送、送信、更新、削除する | [message](../resources/message.md) | [message のメソッド](../resources/message.md#methods) |
| メールボックス所有者の代理としてメッセージを送信するように別のユーザーに委任する | [message](../resources/message.md) | [メッセージ](../resources/message.md)の **from** プロパティと **sender** プロパティの設定 |
| ユーザーがより重要なメッセージを最初に表示できるようにする | [inferenceClassificationOverride](../resources/inferenceclassificationoverride.md) | [優先受信トレイ](../resources/manage-focused-inbox.md) |
| メッセージの添付ファイルを追加、取得、削除する | [attachment](../resources/attachment.md)、 <br> [fileAttachment](../resources/fileattachment.md)、 <br> [itemAttachment](../resources/itemattachment.md)、 <br> [referenceAttachment](../resources/referenceattachment.md)、 <br> [message](../resources/message.md) | [添付ファイルのメソッド](../resources/attachment.md#methods) |
| ユーザーの自動応答、ロケール、タイム ゾーン、就業時間を取得または更新する | [mailboxSettings](../resources/mailboxsettings.md)、 <br> [automaticRepliesSetting](../resources/automaticrepliessetting.md)、 <br> [localeInfo](../resources/localeinfo.md)、 <br> [workingHours](../resources/workinghours.md) | [ユーザーのメールボックスの設定を取得する](../api/user-get-mailboxsettings.md)、 <br> [ユーザーのメールボックスの設定を更新する](../api/user-update-mailboxsettings.md) |
| 他の受信者の特別な状態、不在時のメール ヒントを取得します。 | [ユーザー](../resources/user.md)、 <br> [メール ヒント](../resources/mailtips.md) | [メール ヒントを取得します。](../api/user-getmailtips.md) |
| **メールとフォルダーの管理** | | |
| メール フォルダー階層内のメッセージを整理する | [mailFolder](../resources/mailfolder.md)  | [mailFolder のメソッド](../resources/mailfolder.md#methods) |
| メッセージの検索とフィルター処理 | [message](../resources/message.md) | [クエリ パラメーター](/graph/query-parameters)  |
| フォルダー内のメッセージに対する変更の通知を受け取る | [subscription](../resources/subscription.md) | [Microsoft Graph の Webhooks での作業](../resources/webhooks.md) |
| メッセージまたはメール フォルダーの階層を同期する | [message](../resources/message.md) | [フォルダー内のメッセージへの増分の変更を取得する](/graph/delta-query-messages) |
| **アプリ開発** | | |
| メッセージのインターネット メッセージのヘッダーとカスタム アプリケーションのデータを追加します。 | [message](../resources/message.md) | メッセージの**internetMessageHeaders**プロパティにカスタム データを追加します。 |
| 拡張機能を使用してカスタム アプリ データをメッセージに追加する | [openTypeExtension](../resources/opentypeextension.md)、 <br>[schemaExtension](../resources/schemaextension.md) | [拡張機能を使用してカスタム データをリソースに追加する](/graph/extensibility-overview) |
| 公開の度合いが不十分の Outlook MAPI プロパティのカスタム データにアクセスする | [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md)、 <br> [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) | [Outlook の拡張プロパティの概要](../resources/extended-properties-overview.md) |

## <a name="next-steps"></a>次の手順

メール API は、ユーザーと連携するための新しい方法を開発することができます。

- [Outlook メール API の概要](/graph/outlook-mail-concept-overview)
- [message](../resources/message.md) リソースと [mailFolder](../resources/mailfolder.md) リソースの[メソッド](../resources/message.md#methods)、[プロパティ](../resources/message.md#properties)、[リレーションシップ](../resources/message.md#relationships)について詳しく説明します。
- [Graph エクスプローラー](https://developer.microsoft.com/graph/graph-explorer)で API をお試しください。

さらに情報が必要な場合「[パートナーによる Microsoft Graph の活用方法](https://developer.microsoft.com/graph/graph/examples#partners)」を参照してください。