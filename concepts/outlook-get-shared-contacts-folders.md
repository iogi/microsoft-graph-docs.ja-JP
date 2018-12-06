---
title: 共有フォルダー内にある Outlook の連絡先を取得する
description: " 別名 "
ms.openlocfilehash: c8c5b3a2eac49153826113af036146cc4475d9e5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092404"
---
# <a name="get-outlook-contacts-in-a-shared-folder"></a>共有フォルダー内にある Outlook の連絡先を取得する

Outlook では、ユーザーがフォルダーを互いに共有し、個々の連絡先フォルダーに対する "読み取り"、"作成"、"変更"、"削除" のアクセス権を与えることができます。 また、Outlook では、あるユーザーが別のユーザーの代理人としてふるまい、ユーザーのメールボックス全体の中にある特定のフォルダーにアクセスすることもできます。これは Outlook では "委任" とも呼ばれます。

Microsoft Graph では、他のユーザーによって共有された連絡先フォルダーの連絡先を取得したり、共有フォルダー自体を取得したりする機能がプログラムとしてサポートされています。 また、委任メールボックスのフォルダーにもサポートが適用されます。

たとえば、Garth が John とカスタム連絡先フォルダーを共有し、John に読み取りアクセス権を与えたとします。 John がアプリにサインインし、委任されたアクセス許可 (Contacts.Read.Shared または Contacts.ReadWrite.Shared) を与えた場合、アプリでは、下記のようにして Garth のカスタム連絡先フォルダーと、そのフォルダー内にある連絡先にアクセスすることができます。

## <a name="get-a-contact-in-the-shared-folder"></a>共有フォルダー内の連絡先を取得

Garth が John と共有したカスタム連絡先フォルダーの特定の連絡先を取得できます。

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts/{id}
```

正常に終了すると、HTTP 200 OK となり、Garth の共有連絡先フォルダー`{id}`によって識別される[連絡先](/graph/api/resources/contact?view=graph-rest-1.0)インスタンスが取得されます。

## <a name="get-all-contacts-in-the-shared-folder"></a>共有フォルダー内の全連絡先を取得

Garth の共有フォルダー内の全連絡先を取得します。

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts
```

正常に終了すると、HTTP 200 OK となり、Garth の共有連絡先フォルダーにある[連絡先](/graph/api/resources/contact?view=graph-rest-1.0)インスタンスのコレクションが取得されます。

## <a name="get-the-shared-folder"></a>共有フォルダーを取得

Garth が John と共有した連絡先フォルダーを取得します。

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}
```

正常に終了すると、HTTP 200 OK となり、Garth の共有連絡先フォルダーを表す [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) インスタンスを取得します。

Garth が John に対して自分のメールボックス全体を John に委任していた場合も、同じ GET 機能が適用されます。

Garth が John と連絡先フォルダーを共有しておらず、自分のメールボックスを John に委任していない場合、それらの GET 操作に Garth のユーザー ID またはユーザー プリンシパル名を指定すると、エラーが返されます。 


## <a name="next-steps"></a>次のステップ

詳細情報:

- [Outlook 個人用連絡先を統合する理由](outlook-contacts-concept-overview.md)
- Microsoft Graph v1.0 の[連絡先](/graph/api/resources/contact?view=graph-rest-1.0) API。