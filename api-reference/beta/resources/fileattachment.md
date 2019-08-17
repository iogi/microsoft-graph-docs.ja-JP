---
title: fileAttachment リソースの種類
description: イベントに添付されたファイル (テキストファイルや Word 文書など)
localization_priority: Normal
doc_type: resourcePageType
ms.prod: outlook
author: angelgolfer-ms
ms.openlocfilehash: 7161d8bf17aa573cad61123200785ff254c24feb
ms.sourcegitcommit: 36066afdced00f32838a03747d3e7760fc43683a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2019
ms.locfileid: "36453156"
---
# <a name="fileattachment-resource-type"></a>fileAttachment リソースの種類

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

[イベント](../resources/event.md)、[メッセージ](../resources/message.md)、 [Outlook タスク](../resources/outlooktask.md)、または[投稿](../resources/post.md)に添付されたファイル (テキストファイルや Word 文書など)。 **Contentbytes**プロパティには、ファイルの base64 でエンコードされたコンテンツが含まれています。  

添付ファイルを作成する場合は、要求本文に以下が含まれます。

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* 必要なプロパティ **name** と **contentBytes**。

[添付ファイル](attachment.md)から派生します。

## <a name="methods"></a>メソッド

| メソッド       | 戻り値の型  |説明|
|:---------------|:--------|:----------|
|[取得](../api/attachment-get.md) | [fileAttachment](fileattachment.md) |fileattachment オブジェクトのプロパティと関係を読み取ります。|
|[Delete](../api/attachment-delete.md) | None |fileAttachment オブジェクトを削除します。 |

## <a name="properties"></a>プロパティ
| プロパティ     | 型   |説明|
|:---------------|:--------|:----------|
|contentBytes|Edm。バイナリ|base64 でエンコードされたファイルの内容。|
|contentId|String|Exchange ストア内の添付ファイルの ID。|
|contentLocation|String|このプロパティは、サポートされていないため、使用しないでください。|
|contentType|String|添付ファイルのコンテンツ タイプ。|
|id|文字列|添付ファイル ID。|
|isInline|Boolean|インライン添付ファイルの場合、true に設定します。|
|lastModifiedDateTime|DateTimeOffset|添付ファイルが最後に変更された日時です。|
|name|String|埋め込み添付ファイルを表すアイコンの下に表示されるテキストを表す名前。これは、実際のファイル名にする必要はありません。|
|size|Int32|添付ファイルのバイト単位のサイズ。|

## <a name="relationships"></a>関係
なし


## <a name="json-representation"></a>JSON 表記

以下は、リソースの JSON 表記です

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileAttachment"
}-->

```json
{
  "contentBytes": "string (binary)",
  "contentId": "string",
  "contentLocation": "string",
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "fileAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
