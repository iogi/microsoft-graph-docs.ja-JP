---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListInfo
ms.openlocfilehash: fb955a89c8dfb7b399d15f00666f21899abdc33d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27068814"
---
# <a name="listinfo-resource"></a>ListInfo リソース

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

**listInfo** 複合型は、[list][] に関する追加情報を提供します。

[list]: list.md

## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です。

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.listInfo"
}-->

```json
{
  "contentTypesEnabled": false,
  "hidden": false,
  "template": "documentLibrary | genericList | tasks | survey | links | announcements | contacts | ..."
}
```

## <a name="properties"></a>プロパティ

| プロパティ名           | 型    | 説明
|:------------------------|:--------|:------------------------------------------------
| **contentTypesEnabled** | Boolean | `true` である場合、このリストのコンテンツ タイプが有効であることを示します。
| **hidden**              | Boolean | `true` である場合、リストが通常 SharePoint ユーザー エクスペリエンスに表示されないことを示します。
| **template**            | String  | リストの作成に使用される基本リスト テンプレートを表す列挙値。 代入可能な値は `documentLibrary`、`genericList`、`task`、`survey`、`announcements`、`contacts` などです。

### <a name="remarks"></a>備考

ユーザーによって作成されたほとんどのリストには、上記の値のいずれかが含まれますが、それ以外の値を含めることも可能です。
アプリは、ここに記載されていない任意の値も処理できるようになっている必要があります。
SharePoint の CSOM API に詳しい開発者へ: `template` の値は `SPListTemplateType` 列挙体に相当します。

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->