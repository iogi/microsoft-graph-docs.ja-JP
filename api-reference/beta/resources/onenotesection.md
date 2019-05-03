---
title: onenoteSection リソースの種類
description: OneNote ノートブックのセクション。 セクションには、ページを含めることができます。
localization_priority: Normal
ms.openlocfilehash: d262065f46052c1cae55b42babaa91a2e065d3ef
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2019
ms.locfileid: "33348853"
---
# <a name="onenotesection-resource-type"></a>onenoteSection リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

OneNote ノートブックのセクション。 セクションには、ページを含めることができます。

## <a name="properties"></a>プロパティ
| プロパティ     | 種類   |説明|
|:---------------|:--------|:----------|
|createdBy|[identitySet](identityset.md)|そのアイテムを作成したユーザーの ID、デバイス、アプリケーション。読み取り専用です。|
|createdDateTime|DateTimeOffset|セクションが作成された日時。 Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'` 読み取り専用です。|
|id|String|セクションの一意識別子。  読み取り専用です。|
|isDefault|ブール型 (Boolean)|これがユーザーの既定のセクションであるかどうかを示します。 読み取り専用です。|
|lastModifiedBy|[identitySet](identityset.md)|そのアイテムを作成したユーザーの ID、デバイス、アプリケーション。読み取り専用です。|
|lastModifiedDateTime|DateTimeOffset|セクションが最後に変更された日時。 Timestamp は、ISO 8601 形式を使用した日付と時刻の情報を表し、必ず UTC 時間です。 たとえば、2014 年 1 月 1 日午前 0 時 (UTC) は、次のようになります。`'2014-01-01T00:00:00Z'` 読み取り専用です。|
|リンク|[sectionlinks](sectionlinks.md)|セクションを開くためのリンク。 リンク`oneNoteClientURL`によって、OneNote native client のセクションがインストールされている場合は、そのセクションが開きます。 リンク`oneNoteWebURL`によって、OneNote Online のセクションが開きます。|
|displayName|String|セクションの名前。 |
|pagesUrl|String|セクション`pages`内のすべてのページの詳細を取得できるエンドポイント。 読み取り専用です。|
|self|String|セクションに関する詳細を取得できるエンドポイント。 読み取り専用です。|

## <a name="relationships"></a>関係
| リレーションシップ | 型   |説明|
|:---------------|:--------|:----------|
|ページ|[onenotePage](onenotepage.md)コレクション|セクション内のページのコレクションです。  読み取り専用です。 Null 許容型。|
|parentNotebook|[ノートブック](notebook.md)|セクションを含むノートブック。  読み取り専用です。|
|parentSectionGroup|[sectionGroup](sectiongroup.md)|セクションを含むセクショングループ。  値の取得のみ可能です。|

## <a name="methods"></a>メソッド

| メソッド           | 戻り値の型    |説明|
|:---------------|:--------|:----------|
|[セクションを取得する](../api/section-get.md) | [onenoteSection](onenotesection.md) |セクションのプロパティとリレーションシップを読み取ります。|
|[Create page](../api/section-post-pages.md) |[onenotePage](onenotepage.md)| 指定したセクションの pages コレクションへの投稿によってページを作成します。|
|[ページを一覧表示する](../api/section-list-pages.md) |[onenotePage](onenotepage.md)コレクション| 指定したセクション内のページのコレクションを取得します。|
|[copyToNotebook](../api/section-copytonotebook.md)|なし|セクションを特定のノートブックにコピーします。|
|[copyToSectionGroup](../api/section-copytosectiongroup.md)|なし|セクションを特定のセクショングループにコピーします。|


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "pages",
    "parentNotebook",
    "parentSectionGroup"
  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",  
  "@odata.type": "microsoft.graph.onenoteSection"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isDefault": true,
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.sectionLinks"},
  "displayName": "string",
  "pagesUrl": "string",
  "self": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "onenoteSection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->