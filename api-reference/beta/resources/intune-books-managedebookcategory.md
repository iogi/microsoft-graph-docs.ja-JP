---
title: managedEBookCategory リソースの種類
description: 単一の Intune 電子ブックカテゴリのプロパティが含まれています。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: ad1f8c2d4c680ef3594d29a11eb15edcb708b77a
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36335103"
---
# <a name="managedebookcategory-resource-type"></a>managedEBookCategory リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

単一の Intune 電子ブックカテゴリのプロパティが含まれています。

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[ManagedEBookCategories のリスト](../api/intune-books-managedebookcategory-list.md)|[Managedebookcategory](../resources/intune-books-managedebookcategory.md)コレクション|[Managedebookcategory](../resources/intune-books-managedebookcategory.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[ManagedEBookCategory の取得](../api/intune-books-managedebookcategory-get.md)|[managedEBookCategory](../resources/intune-books-managedebookcategory.md)|[Managedebookcategory](../resources/intune-books-managedebookcategory.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[ManagedEBookCategory の作成](../api/intune-books-managedebookcategory-create.md)|[managedEBookCategory](../resources/intune-books-managedebookcategory.md)|新しい[Managedebookcategory](../resources/intune-books-managedebookcategory.md)オブジェクトを作成します。|
|[ManagedEBookCategory の削除](../api/intune-books-managedebookcategory-delete.md)|None|[Managedebookcategory](../resources/intune-books-managedebookcategory.md)を削除します。|
|[ManagedEBookCategory の更新](../api/intune-books-managedebookcategory-update.md)|[managedEBookCategory](../resources/intune-books-managedebookcategory.md)|[Managedebookcategory](../resources/intune-books-managedebookcategory.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|文字列|エンティティのキー。|
|displayName|String|EBook カテゴリの名前を指定します。|
|lastModifiedDateTime|DateTimeOffset|ManagedEBookCategory が最後に変更された日付と時刻。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedEBookCategory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedEBookCategory",
  "id": "String (identifier)",
  "displayName": "String",
  "lastModifiedDateTime": "String (timestamp)"
}
```



