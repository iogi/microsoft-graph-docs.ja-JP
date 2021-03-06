# <a name="contactfolder-resource-type"></a>contactFolder リソース型

連絡先が格納されたフォルダーです。

このリソースでは、[デルタ](../api/contactfolder_delta.md)関数を用意すれば、増分の追加、削除、更新に[デルタ クエリ](../../../concepts/delta_query_overview.md)を使用できます。


## <a name="methods"></a>メソッド

| メソッド       | 戻り値の型  |説明|
|:---------------|:--------|:----------|
|[contactFolder を取得する](../api/contactfolder_get.md) | [contactFolder](contactfolder.md) |連絡先フォルダー ID を使用して連絡先フォルダーを取得します。|
|[更新する](../api/contactfolder_update.md) | [contactFolder](contactfolder.md) |contactFolder オブジェクトを更新します。 |
|[削除](../api/contactfolder_delete.md) | なし |contactFolder オブジェクトを削除します。 |
|[childFolders を一覧表示する](../api/contactfolder_list_childfolders.md) |[ContactFolder](contactfolder.md) collection| 指定した連絡先フォルダーの下の子フォルダーのコレクションを取得します。|
|[子 contactFolder を作成する](../api/contactfolder_post_childfolders.md) |[ContactFolder](contactfolder.md)| 指定したフォルダーの子として新しい contactFolder を作成します。|
|[delta](../api/contact_delta.md)|[contact](contact.md)コレクション| ユーザーのメールボックスで追加または削除された一連の連絡先フォルダーを取得します。|
|[フォルダー内の連絡先を一覧表示する](../api/contactfolder_list_contacts.md) |[Contact](contact.md) collection| サインイン中のユーザーの既定の連絡先フォルダーから連絡先のコレクションを取得する (`.../me/contacts`) か、指定した連絡先フォルダーから取得します。|
|[フォルダー内に連絡先を作成する](../api/contactfolder_post_contacts.md) |[Contact](contact.md)| 連絡先をルート連絡先フォルダーまたは別の連絡先フォルダーの `contacts` エンドポイントに追加します。|
|[単一値の拡張プロパティを作成する](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[contactFolder](contactFolder.md)  |新規または既存の contactFolder に、1 つ以上の単一値の拡張プロパティを作成します。   |
|[単一値の拡張プロパティを持つ contactFolder を取得する](../api/singlevaluelegacyextendedproperty_get.md)  | [contactFolder](contactFolder.md) | `$expand` または `$filter` を使用して、単一値の拡張プロパティを含む contactFolder を取得します。 |
|[複数値の拡張プロパティを作成する](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [contactFolder](contactFolder.md) | 新規または既存の contactFolder に、1 つ以上の複数値の拡張プロパティを作成します。  |
|[複数値の拡張プロパティを持つ contactFolder を取得する](../api/multivaluelegacyextendedproperty_get.md)  | [contactFolder](contactFolder.md) | `$expand` を使用して、複数値の拡張プロパティを含む contactFolder を取得します。 |

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|displayName|String|フォルダーの表示名。|
|id|String|連絡先フォルダーの一意識別子。読み取り専用。|
|parentFolderId|String|フォルダーの親フォルダーの ID。|

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|childFolders|[ContactFolder](contactfolder.md) コレクション|フォルダー内の子フォルダーのコレクション。ナビゲーション プロパティ。読み取り専用。Null 許容型。|
|contacts|[Contact](contact.md) コレクション|フォルダー内の連絡先。ナビゲーション プロパティ。読み取り専用。Null 許容型。|
|multiValueExtendedProperties|[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) コレクション| contactFolder に定義された、複数値の拡張プロパティのコレクションです。読み取り専用。Null 許容型。|
|singleValueExtendedProperties|[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) コレクション| contactFolder に定義された、単一値の拡張プロパティのコレクションです。読み取り専用。Null 許容型。|

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "contacts",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.contactFolder"
}-->

```json
{
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string"
}

```

## <a name="see-also"></a>関連項目

- [デルタ クエリを使用して、Microsoft Graph データの変更を追跡する](../../../concepts/delta_query_overview.md)
- [フォルダー内のメッセージへの増分の変更を取得する](../../../concepts/delta_query_messages.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contactFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
