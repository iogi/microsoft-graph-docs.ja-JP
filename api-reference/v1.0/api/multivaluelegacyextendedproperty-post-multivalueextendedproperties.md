---
title: 複数値の拡張プロパティを作成する
description: 'リソースの新規または既存のインスタンスに、1 つ以上の複数値の拡張プロパティを作成します。 '
ms.openlocfilehash: 2eb3c337b89be8dc6109dc26de35fcaea88d6609
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27024135"
---
# <a name="create-multi-value-extended-property"></a>複数値の拡張プロパティを作成する

リソースの新規または既存のインスタンスに、1 つ以上の複数値の拡張プロパティを作成します。 

次のユーザー リソースがサポートされます。

- [calendar](../resources/calendar.md)
- [contact](../resources/contact.md)
- [contactFolder](../resources/contactfolder.md) 
- [イベント](../resources/event.md)
- [mailFolder](../resources/mailfolder.md)
- [message](../resources/message.md)

次のグループ リソースもサポートされます。

- グループ [calendar](../resources/calendar.md)
- グループ [event](../resources/event.md)
- グループ [post](../resources/post.md) 

オープン拡張機能または拡張プロパティを使用するのに適した状況と、拡張プロパティを指定する方法の詳細については、「[拡張プロパティの概要](../resources/extended-properties-overview.md)」を参照してください。

## <a name="permissions"></a>アクセス許可
リソースに応じて、[拡張プロパティを作成するアクセス許可が委任された (アプリケーション) を要求を入力、次の表で指定されたアクセス許可は、この API を呼び出すために必要最低限。 アクセス許可の選択方法などの詳細については、「[アクセス許可](/graph/permissions-reference)」を参照してください。

| サポートされているリソース | 委任 (職場または学校のアカウント) | 委任 (個人用 Microsoft アカウント) | アプリケーション |
|:-----|:-----|:-----|:-----|
| [calendar](../resources/calendar.md) | Calendars.ReadWrite | Calendars.ReadWrite | Calendars.ReadWrite |
| [連絡先](../resources/contact.md) | Contacts.ReadWrite | Contacts.ReadWrite | Contacts.ReadWrite |
| [contactFolder](../resources/contactfolder.md) | Contacts.ReadWrite | Contacts.ReadWrite | Contacts.ReadWrite |
| [イベント](../resources/event.md) | Calendars.ReadWrite | Calendars.ReadWrite |  Calendars.ReadWrite|
| グループ [calendar](../resources/calendar.md) | Group.ReadWrite.All | 使用不可 | 使用不可 |
| グループ [event](../resources/event.md) | Group.ReadWrite.All | 使用不可 | 使用不可 |
| グループ [post](../resources/post.md) | Group.ReadWrite.All | 使用不可 | 使用不可 |
| [mailFolder](../resources/mailfolder.md) | Mail.ReadWrite | Mail.ReadWrite | Mail.ReadWrite |
| [メッセージ](../resources/message.md) | Mail.ReadWrite | Mail.ReadWrite | Mail.ReadWrite |

## <a name="http-request"></a>HTTP 要求
新規または既存のリソースのインスタンスに、拡張プロパティを作成できます。

1 つ以上の拡張プロパティを_新しい_リソースのインスタンスに作成するには、インスタンスの作成と同じ REST 要求を使用し、新しいリソース インスタンスのプロパティ_と拡張プロパティを_要求の本文に含めます。一部のリソースでは複数の作成方法がサポートされていますので、注意してください。これらのリソース インスタンスの作成に関して詳しくは、[メッセージ](../resources/message.md)、[mailFolder](../api/user-post-mailfolders.md)、[イベント](../api/user-post-events.md)、[予定表](../api/user-post-calendars.md)、[連絡先](../api/user-post-contacts.md)、[contactFolder](../api/user-post-contactfolders.md)、[グループ イベント](../api/group-post-events.md)、および [グループ投稿](../resources/post.md)作成の該当する各トピックをご覧ください。 
 
以下に要求の構文を示します。 

<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages

POST /me/mailFolders
POST /users/{id|userPrincipalName}/mailFolders

POST /me/events
POST /users/{id|userPrincipalName}/events

POST /me/calendars
POST /users/{id|userPrincipalName}/calendars

POST /me/contacts
POST /users/{id|userPrincipalName}/contacts

POST /me/contactFolders
POST /users/{id|userPrincipalName}/contactFolders

POST /groups/{id}/events

POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
POST /groups/{id}/threads
POST /groups/{id}/conversations
```

既存のリソースのインスタンスで 1 つ以上の拡張プロパティを作成するには、要求でインスタンスを指定し、要求本文に拡張プロパティを含めます。

**注** 既存のグループ投稿には拡張プロパティを作成できません。

<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id|userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}

PATCH /me/mailFolders/{id}
PATCH /users/{id|userPrincipalName}/mailFolders/{id}

PATCH /me/events/{id}
PATCH /users/{id|userPrincipalName}/events/{id}

PATCH /me/calendars/{id}
PATCH /users/{id|userPrincipalName}/calendars/{id}

PATCH /me/contacts/{id}
PATCH /users/{id|userPrincipalName}/contacts/{id}

PATCH /me/contactFolders/{id}
PATCH /users/{id|userPrincipalName}/contactFolders/{id}

PATCH /groups/{id}/events/{id}
```

## <a name="request-headers"></a>要求ヘッダー
| 名前       | 値 |
|:---------------|:----------|
| Authorization | ベアラー {トークン}。必須。 |
| Content-Type | application/json |

## <a name="request-body"></a>要求本文

リソース インスタンスの **multiValueExtendedProperties** コレクション プロパティに、各 [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) オブジェクトの JSON 本文を指定します。

|プロパティ|型|説明|
|:-----|:-----|:-----|
|multiValueExtendedProperties|[multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) collection| 1 つ以上の複数値を持つ拡張プロパティの配列。 |
|id|String|**multiValueExtendedProperties** コレクションの各プロパティに対してこれを指定し、プロパティを特定します。サポートされている形式のいずれかに従う必要があります。詳しくは、[「Outlook の拡張プロパティの概要」](../resources/extended-properties-overview.md)をご覧ください。必須。|
|value|文字列|**multiValueExtendedProperties** コレクションの各プロパティに対し、プロパティの値を特定します。必須。|

だけでなく、新しい**multiValueExtendedProperties**コレクションの_新しい_リソースのインスタンスで拡張プロパティを作成するときにそのリソースのインスタンスにも (つまり、[メッセージ](../resources/message.md)、 [mailFolder の JSON 表現を提供します。](../resources/mailfolder.md)、[イベント](../resources/event.md)などです。)。


## <a name="response"></a>応答

#### <a name="response-code"></a>応答コード
新しいリソース インスタンスに拡張プロパティが正常に作成されると、`201 Created` が返されます。ただし新しいグループ投稿の場合は別で、使用するメソッドに応じて、`200 OK` または `202 Accepted` が返されます。

既存のリソース インスタンスに拡張プロパティが正常に作成されると、`200 OK` が返されます。 


#### <a name="response-body"></a>応答本文

[グループ投稿](../resources/post.md)以外のサポートされているリソースで拡張プロパティを作成する場合、応答には新規または既存のインスタンスだけが含まれ、新しい拡張プロパティは含まれません。新しく作成された拡張プロパティを表示するには、[拡張プロパティを使用して展開されているインスタンスを取得](../api/multivaluelegacyextendedproperty-get.md)します。

_新しい_グループ投稿に拡張プロパティを作成する場合、応答には応答コードだけが含まれ、新しい投稿や拡張プロパティは含まれません。既存のグループ投稿には拡張プロパティを作成できません。


## <a name="example"></a>例
##### <a name="request-1"></a>要求 1

最初の例では、すべて同じ POST 操作の新しいイベントで複数値の拡張プロパティを作成します。新しいイベントに通常含まれるプロパティとは別に、要求の本文に 1 つの拡張プロパティを含む **multiValueExtendedProperties** コレクションが含まれます。要求本文には、その複数値の拡張プロパティに関する次のものが含まれています。

- **id** 指定された GUID と名前 `Recreation` の文字列の配列としてプロパティを指定します。 
- **value** は、3 つの文字列値 `["Food", "Hiking", "Swimming"]` の配列として `Recreation` を指定します。
 

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/events
Content-Type: application/json

{
  "subject": "Family reunion",
  "body": {
    "contentType": "HTML",
    "content": "Let's get together this Thanksgiving!"
  },
  "start": {
      "dateTime": "2015-11-26T09:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2015-11-29T21:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "attendees": [
    {
      "emailAddress": {
        "address": "Terrie@contoso.com",
        "name": "Terrie Barrera"
      },
      "type": "Required"
    },
    {
      "emailAddress": {
        "address": "Lauren@contoso.com",
        "name": "Lauren Solis"
      },
      "type": "Required"
    }
  ],
  "multiValueExtendedProperties": [
     {
           "id":"StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation",
           "value": ["Food", "Hiking", "Swimming"]
     }
  ]
}
```

##### <a name="response-1"></a>応答 1

[イベントのみの作成](../api/user-post-events.md)からの応答と同様に、`HTTP 201 Created` 応答コードによって正常な応答が示され、応答の本文に新しいイベントが含まれます。応答には、新しく作成された拡張プロパティは含まれません。

新しく作成された拡張プロパティを表示するには、[拡張プロパティを使用して展開されているイベントを取得](../api/multivaluelegacyextendedproperty-get.md)します。


****

##### <a name="request-2"></a>要求 2

2 番目の例では、指定したメッセージに対して 1 つの複数値の拡張プロパティを作成します。拡張プロパティは、**multiValueExtendedProperties** コレクションの唯一の要素です。要求本文には、拡張プロパティに関する次のものが含まれています。

- **id** 指定された GUID と名前 `Palette` を使って、文字列の配列としてプロパティを指定します。
- **value** 3 つの文字列値 `["Green", "Aqua", "Blue"]` の配列として `Palette` を指定します。

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2_as77AACHsLrBBBA=')

Content-Type: application/json

{
  "multiValueExtendedProperties": [
      {
         "id":"StringArray {66f5a359-4659-4830-9070-00049ec6ac6e} Name Palette",
         "value":["Green", "Aqua", "Blue"]
      }
    ]
}
```

##### <a name="response-2"></a>応答 2

[メッセージの更新](../api/message-update.md)からの応答と同様に、`HTTP 200 OK` 応答コードによって正常な応答が示され、応答の本文に指定したメッセージが含まれています。応答には、新しく作成された拡張プロパティは含まれません。

新しく作成された拡張プロパティを表示するには、[拡張プロパティを使用して展開されているメッセージを取得](../api/multivaluelegacyextendedproperty-get.md)します。


<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create a single-value extended property",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->



