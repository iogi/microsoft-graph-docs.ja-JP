# <a name="educationroot-resource-type"></a>educationRoot リソースの種類

`/education` 名前空間は、教育機関に固有の機能を公開します。 `/education` 名前空間の一部のオブジェクトは、Microsoft Graph の別の部分 (たとえば、[users](user.md)) にあります。 教育機関の名前空間は、これらのオブジェクトに教育機関固有のプロパティと機能を提供します。

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[Create educationClass](../api/educationroot_post_classes.md) |[educationClass](educationclass.md)| クラス コレクションに投稿して、新しい **educationClass** を作成します。|
|[List classes](../api/educationroot_list_classes.md) |[educationClass](educationclass.md) コレクション| **educationClass** オブジェクト コレクションを取得します。|
|[Create educationSchool](../api/educationroot_post_schools.md) |[educationSchool](educationschool.md)| 学校コレクションに投稿して、新しい **educationSchool** を作成します。|
|[List schools](../api/educationroot_list_schools.md) |[educationSchool](educationschool.md) コレクション| **educationSchool** オブジェクト コレクションを取得します。|
|[Create educationUser](../api/educationroot_post_users.md) |[educationUser](educationuser.md)| ユーザー コレクションに投稿して、新しい **educationUser** を作成します。|
|[List users](../api/educationroot_list_users.md) |[educationUser](educationuser.md) コレクション| **educationUser** オブジェクト コレクションを取得します。|

## <a name="properties"></a>プロパティ
なし

## <a name="relationships"></a>リレーションシップ
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|classes|[educationClass](educationclass.md) コレクション| 読み取り専用。Null 許容型。|
|me|[educationUser](educationuser.md)| 読み取り専用。Null 許容型。|
|schools|[educationSchool](educationschool.md) コレクション| 読み取り専用。Null 許容型。|
|users|[educationUser](educationuser.md) コレクション| 読み取り専用。Null 許容型。|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationRoot resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->