---
title: deviceManagementCollectionSettingInstance リソースの種類
description: 値のコレクションを表す設定インスタンス
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: b569bb4d0b38eb3fd9c3909d559e3066b4ccae6f
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36365420"
---
# <a name="devicemanagementcollectionsettinginstance-resource-type"></a>deviceManagementCollectionSettingInstance リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

値のコレクションを表す設定インスタンス


[Devicemanagementsettinginstance](../resources/intune-deviceintent-devicemanagementsettinginstance.md)から継承します

## <a name="methods"></a>メソッド
|メソッド|戻り値の型|説明|
|:---|:---|:---|
|[DeviceManagementCollectionSettingInstances を一覧表示する](../api/intune-deviceintent-devicemanagementcollectionsettinginstance-list.md)|[Devicemanagementcollectionsettinginstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)コレクション|[Devicemanagementcollectionsettinginstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)オブジェクトのプロパティとリレーションシップをリストします。|
|[DeviceManagementCollectionSettingInstance を取得する](../api/intune-deviceintent-devicemanagementcollectionsettinginstance-get.md)|[deviceManagementCollectionSettingInstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)|[Devicemanagementcollectionsettinginstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)オブジェクトのプロパティとリレーションシップを読み取ります。|
|[DeviceManagementCollectionSettingInstance の作成](../api/intune-deviceintent-devicemanagementcollectionsettinginstance-create.md)|[deviceManagementCollectionSettingInstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)|新しい[Devicemanagementcollectionsettinginstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)オブジェクトを作成します。|
|[DeviceManagementCollectionSettingInstance の削除](../api/intune-deviceintent-devicemanagementcollectionsettinginstance-delete.md)|None|[Devicemanagementcollectionsettinginstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)を削除します。|
|[DeviceManagementCollectionSettingInstance の更新](../api/intune-deviceintent-devicemanagementcollectionsettinginstance-update.md)|[deviceManagementCollectionSettingInstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)|[Devicemanagementcollectionsettinginstance](../resources/intune-deviceintent-devicemanagementcollectionsettinginstance.md)オブジェクトのプロパティを更新します。|

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|id|String|[Devicemanagementsettinginstance](../resources/intune-deviceintent-devicemanagementsettinginstance.md)から継承された設定インスタンス ID|
|definitionId|String|[Devicemanagementsettinginstance](../resources/intune-deviceintent-devicemanagementsettinginstance.md)から継承されたこのインスタンスの設定定義の ID|
|valueJson|String|[Devicemanagementsettinginstance](../resources/intune-deviceintent-devicemanagementsettinginstance.md)から継承された値の JSON 表現|

## <a name="relationships"></a>リレーションシップ
|リレーションシップ|型|説明|
|:---|:---|:---|
|value|[Devicemanagementsettinginstance](../resources/intune-deviceintent-devicemanagementsettinginstance.md)コレクション|値のコレクション|

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementCollectionSettingInstance"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementCollectionSettingInstance",
  "id": "String (identifier)",
  "definitionId": "String",
  "valueJson": "String"
}
```



