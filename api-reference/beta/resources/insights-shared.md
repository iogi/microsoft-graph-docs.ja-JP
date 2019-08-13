---
title: /リソースの種類 (Sharepoint)
description: または特定のユーザーによって共有されているファイルを表す洞察。 次の共有ファイルがサポートされています。
author: simonhult
localization_priority: Normal
ms.prod: insights
doc_type: resourcePageType
ms.openlocfilehash: e95a7a54d2cdce7e23bcc4792368cfa250241963
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36366351"
---
# <a name="sharedinsight-resource-type"></a>/リソースの種類 (Sharepoint)

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

または特定のユーザーによって共有されているファイルを表す洞察。 次の共有ファイルがサポートされています。

- 電子メールまたは会議の招待に直接添付されたファイル。
- OneDrive for Business および SharePoint のモダン添付ファイル-ユーザーが電子メールのリンクとして共有する、OneDrive for business および SharePoint に格納されているファイル。

**注**: 現在、データを使用して共有 API の結果を設定する作業を行っています。 リリース後の最初の週に、一部のデータが欠落している場合があります。

## <a name="methods"></a>メソッド

| メソッド       | 戻り値の型  |説明|
|:---------------|:--------|:----------|
|[共有リスト](../api/insights-list-shared.md) |[insights_shared](insights-shared.md)コレクション| 共有ファイルの一覧を取得します。|

## <a name="properties"></a>プロパティ

| プロパティ              | 型                      | 説明  |
| -------------         |---------------            | -------------|
| id                    | String                    | リレーションシップの一意識別子。 読み取り専用です。        |
| lastShared            | [sharingDetail](insights-sharingdetail.md)                | 共有アイテムの詳細。 読み取り専用です。        |
| resourceVisualization | [resourceVisualization](insights-resourcevisualization.md)                | ユーザーの作業でドキュメントをビジュアル化するために使用できるプロパティ。 読み取り専用      |
| resourceReference     | [resourceReference](insights-resourcereference.md)                      | ドキュメントの url や種類など、共有ドキュメントの参照プロパティ。 読み取り専用       |

## <a name="relationships"></a>リレーションシップ

| プロパティ      | 型          | 説明  |
| ------------- |---------------| -------------|
| リソース      | entity コレクション | 共有されているアイテムに移動するために使用します。 添付ファイルの場合、type は*Fileattachment*になります。 リンクされた添付ファイルの場合、種類は [*ドライブ] 項目*です。 |

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です
<!--{
  "blockType":"resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.sharedInsight"
}-->
```json
{
  "id": "string",
  "lastShared": "sharingDetail",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```
