---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Site
ms.openlocfilehash: db465f93f336a51d862daf6e05b1d6bc422247ea
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2017
---
# <a name="site-resource"></a>Site リソース

**サイト** リソースは、メタデータと SharePoint サイトのリレーションシップを提供します。

## <a name="tasks"></a>タスク

以下のすべての例は、`https://graph.microsoft.com/v1.0` からの相対指定です。

| タスク名                | 要求の例
|:-------------------------|:--------------------------------------------------
| [ルート サイトを取得する][]        | GET /sites/root
| [サイトを取得する][]             | GET /sites/{site-id}
| [パスを使用してサイトを取得する][]     | GET /sites/{hostname}:/{site-path}
| [グループのサイトを取得する][] | GET /groups/{group-id}/sites/root
| [サイトを検索する][]     | GET /sites?search={query}

[サイトを取得する]: ../api/site_get.md
[ルート サイトを取得する]: ../api/site_get.md
[パスを使用してサイトを取得する]: ../api/site_getbypath.md
[グループのサイトを取得する]: ../api/site_get.md
[サイトを検索する]: ../api/site_search.md

## <a name="json-representation"></a>JSON 表記

以下は、**サイト** リソースの JSON 表記です。

**driveItem** リソースは [**baseItem**](baseitem.md) から派生し、そのリソースからプロパティを継承します。

<!-- { "blockType": "resource",
       "@odata.type": "microsoft.graph.site",
       "keyProperty": "id",
       "optionalProperties": [ "root", "sharepointIds", "siteCollection", "drive", "drives", "sites" ] } -->

```json
{
  "id": "string",
  "root": { "@odata.type": "microsoft.graph.root" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "siteCollection": {"@odata.type": "microsoft.graph.siteCollection"},
  "displayName": "string",

  /* relationships */
  "contentTypes": [ { "@odata.type": "microsoft.graph.contentType" }],
  "drive": { "@odata.type": "microsoft.graph.drive" },
  "drives": [ { "@odata.type": "microsoft.graph.drive" }],
  "items": [ { "@odata.type": "microsoft.graph.baseItem" }],
  "lists": [ { "@odata.type": "microsoft.graph.list" }],
  "sites": [ { "@odata.type": "microsoft.graph.site"} ],
  "columns": [ { "@odata.type": "microsoft.graph.columnDefinition" }],
  "onenote": [ { "@odata.type": "microsoft.graph.onenote"} ],

  /* inherited from baseItem */
  "name": "string",
  "createdDateTime": "datetime",
  "description": "string",
  "eTag": "string",
  "lastModifiedDateTime": "datetime",
  "webUrl": "url"
}
```

## <a name="properties"></a>プロパティ

| プロパティ名            | 種類                                | 説明                                                                                    |
| :----------------------- | :---------------------------------- | :--------------------------------------------------------------------------------------------- |
| **id**                   | string                              | アイテムの一意識別子。読み取り専用です。                                                  |
| **createdDateTime**      | DateTimeOffset                      | アイテムが作成された日時。読み取り専用です。                                             |
| **説明**          | string                              | サイトの説明テキスト。                                                             |
| **displayName**          | string                              | サイトの完全なタイトル。読み取り専用です。                                                        |
| **lastModifiedDateTime** | DateTimeOffset                      | アイテムが最後に変更された日時。読み取り専用です。                                       |
| **name**                 | string                              | アイテムの名前/タイトル。                                                                  |
| **root**                 | [root](root.md)                     | 存在する場合は、これがサイト コレクションのルート サイトであることを示します。読み取り専用です。            |
| **sharepointIds**        | [sharepointIds](sharepointids.md)   | SharePoint REST 互換性に役立つ識別子を返します。読み取り専用です。                       |
| **siteCollection**       | [siteCollection](sitecollection.md) | サイトのサイト コレクションに関する詳細情報を提供します。ルート サイトにのみ使用できます。読み取り専用です。 |
| **webUrl**               | string (URL)                        | ブラウザーでアイテムを表示する URL。読み取り専用です。                                          |

## <a name="relationships"></a>リレーションシップ

| リレーションシップ名 | 種類                             | 説明
|:------------------|:---------------------------------|:----------------------
| **columns**       | Collection([columnDefinition][]) | このサイトのすべてのリストで再利用可能なコラム定義のコレクションです。
| **contentTypes**  | Collection([contentType][])      | このサイトに定義されたコンテンツ タイプのコレクションです。
| **drive**         | [ドライブ][]                        | このサイトの既定ドライブ (ドキュメント ライブラリ)。
| **ドライブ**        | Collection([drive][])            | このサイトの下のドライブ (ドキュメント ライブラリ) のコレクション。
| **アイテム**         | Collection([baseItem][])         | このサイトに含まれるすべてのアイテムを処理するために使用されました。このコレクションを列挙することはできません。
| **lists**         | Collection([list][])             | このサイトにあるリストのコレクションです。
| **sites**         | Collection([site][])             | このサイトの下のサブサイトのコレクション。
| **onenote**       | [onenote][]                      | ノートブック関連の操作のために OneNote サービスを呼び出します。

[columnDefinition]: columndefinition.md
[baseItem]: baseitem.md
[contentType]: contentType.md
[drive]: drive.md
[identitySet]: identityset.md
[list]: list.md
[site]: site.md
[onenote]: onenote.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Sites",
  "tocBookmarks": { "Resources/Site": "#" }
} -->
