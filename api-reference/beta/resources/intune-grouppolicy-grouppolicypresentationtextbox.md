---
title: groupPolicyPresentationTextBox リソースの種類
description: ADMX textBox 要素と ADMX テキスト要素を表します。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 3f600613cc3d7bf0a1c4be50d63b12863792759e
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36331302"
---
# <a name="grouppolicypresentationtextbox-resource-type"></a>groupPolicyPresentationTextBox リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

ADMX textBox 要素と ADMX テキスト要素を表します。


[GroupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)から継承します。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[GroupPolicyPresentationTextBoxes テキストボックスのリスト](../api/intune-grouppolicy-grouppolicypresentationtextbox-list.md)|[Grouppolicypresentationtextbox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)コレクション|[Grouppolicypresentationtextbox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[GroupPolicyPresentationTextBox の取得](../api/intune-grouppolicy-grouppolicypresentationtextbox-get.md)|[groupPolicyPresentationTextBox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)|[Grouppolicypresentationtextbox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[GroupPolicyPresentationTextBox の作成](../api/intune-grouppolicy-grouppolicypresentationtextbox-create.md)|[groupPolicyPresentationTextBox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)|新しい[Grouppolicypresentationtextbox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)オブジェクトを作成します。|
|[GroupPolicyPresentationTextBox の削除](../api/intune-grouppolicy-grouppolicypresentationtextbox-delete.md)|None|[Grouppolicypresentationtextbox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)を削除します。|
|[GroupPolicyPresentationTextBox の更新](../api/intune-grouppolicy-grouppolicypresentationtextbox-update.md)|[groupPolicyPresentationTextBox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)|[Grouppolicypresentationtextbox](../resources/intune-grouppolicy-grouppolicypresentationtextbox.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|label|String|任意のプレゼンテーションエンティティのローカライズされたテキストラベル。 既定値は空白です。 [GroupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)から継承します。|
|id|String|エンティティのキー。 [GroupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)から継承します。|
|lastModifiedDateTime|DateTimeOffset|エンティティが最後に変更された日付と時刻。 [GroupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)から継承します。|
|defaultValue|String|テキストボックスに表示されるローカライズされた既定の文字列。 既定値は空白です。|
|必須|Boolean|テキストボックスに値を入力する必要があります。 既定値は False です。|
|maxLength|Int64|テキストの最大文字数を指定する符号なし整数。 既定値は1023です。|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|definition|[groupPolicyDefinition](../resources/intune-grouppolicy-grouppolicydefinition.md)|プレゼンテーションに関連付けられたグループポリシーの定義。 [GroupPolicyPresentation](../resources/intune-grouppolicy-grouppolicypresentation.md)から継承します。|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.groupPolicyPresentationTextBox"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.groupPolicyPresentationTextBox",
  "label": "String",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "defaultValue": "String",
  "required": true,
  "maxLength": 1024
}
```



