---
title: fileSecurityState リソースの種類
description: アラートに関連するファイル (プロセスではない) に関する情報が含まれています。
ms.openlocfilehash: d1358d7fe0d5565845201781e32b3da14a89f412
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27023989"
---
# <a name="filesecuritystate-resource-type"></a>fileSecurityState リソースの種類

アラートに関連するファイル (プロセスではない) に関する情報が含まれています。

## <a name="properties"></a>プロパティ

| プロパティ   | 型|説明|
|:---------------|:--------|:----------|
|fileHash|[fileHash](filehash.md)|複合型の暗号化などの場所に依存したファイルのハッシュが含まれています。|
|名前|String|ファイルの名前 (パス) です。|
|path|String|ファイルとイメージ ファイルのファイルの完全パスです。|
|riskScore|String|プロバイダー生成された計算されるリスクの警告ファイルのスコアです。 0 - 1 パーセントに相当する値の範囲をお勧めします。|

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileSecurityState"
}-->

```json
{
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "name": "String",
  "path": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->