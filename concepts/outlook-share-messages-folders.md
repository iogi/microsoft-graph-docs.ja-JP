# <a name="share-outlook-message-folders-between-users"></a>複数ユーザー間での Outlook メッセージ フォルダー共有

<!-- remove similar content in other topics when ready to publish - list messages, get message, get mail folder.
These topics also have similar section - list events, get event, get calendar, list contacts, get contact, get contact folder.
-->

Outlook では、ユーザーがフォルダーを互いに共有し、個々のフォルダーやメールボックス全体に対する「読み取り」、「作成」、「変更」のアクセス権を提供することができます。 これは Outlook で「委任」とも呼ばれています。

Microsoft Graph では、他のユーザーと共有するメール フォルダーのメッセージを取得したり、共有フォルダー自体を取得したりする機能がプログラムとしてサポートされています。

たとえば、Garth が John と、Garth の受信トレイへの読み取りアクセスを共有したとします。 John がアプリにサインインし、委任されたアクセス許可 (Mail.Read.Shared または Mail.ReadWrite.Shared) を提供した場合、アプリでは、下記のようにして Garth のメールおよび Garth の受信トレイにアクセスすることができます。

## <a name="get-a-message-in-the-shared-folder"></a>共有フォルダーのメッセージを取得

Garth の受信トレイの特定のメッセージを取得できます:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages/{id}
```

正常に終了した場合、HTTP 200 OK となり、Garth の受信トレイから `{id}` によって識別される[メッセージ](../api-reference/v1.0/resources/message.md) インスタンスを取得します。

## <a name="get-all-messages-in-the-shared-folder"></a>共有フォルダー内の全メッセージを取得

Garth の受信トレイの全メッセージを取得:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages
```

正常に終了すると、HTTP 200 OK となり、Garth の受信トレイの[メッセージ](../api-reference/v1.0/resources/message.md) インスタンスのコレクションを取得します。

## <a name="get-the-shared-folder"></a>共有フォルダーを取得

Garth が John と共有したフォルダー (受信トレイ) を取得します。

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')
```

正常に終了すると、HTTP 200 OK となり、Garth の受信トレイ フォルダーを表す [mailFolder](../api-reference/v1.0/resources/mailfolder.md) インスタンスを取得します。

Garth が John に対して、Garth の受信トレイへのさらに多くのアクセス権を委任していた場合、または Garth が自分のメールボックス全体を John に委任していた場合も、同じ GET 機能が適用されます。

Garth が John とメッセージ フォルダーを共有していない、もしくはメールボックスを John に委任していない場合、それらの GET 操作に Garth のユーザー ID またはユーザー プリンシパル名を指定すると、エラーが返されます。 


## <a name="next-steps"></a>次の手順

詳細情報:

- [Outlook メールと統合する理由](outlook-mail-concept-overview.md)
- Microsoft Graph v1.0 の[メール API](../api-reference/v1.0/resources/mail_api_overview.md) とその[用途](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases)