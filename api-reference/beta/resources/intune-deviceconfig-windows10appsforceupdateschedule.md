---
title: windows10AppsForceUpdateSchedule リソースの種類
description: アプリの Windows 10 強制更新スケジュール
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: resourcePageType
ms.openlocfilehash: 856729bbdaa9b178a8b7bf31feac58fc39436066
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36337967"
---
# <a name="windows10appsforceupdateschedule-resource-type"></a>windows10AppsForceUpdateSchedule リソースの種類

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

アプリの Windows 10 強制更新スケジュール

## <a name="properties"></a>プロパティ
|プロパティ|型|説明|
|:---|:---|:---|
|startDateTime|DateTimeOffset|強制再起動の開始時刻。|
|recurrence|[windows10AppsUpdateRecurrence](../resources/intune-deviceconfig-windows10appsupdaterecurrence.md)|定期的なスケジュール。 使用可能な値は、`none`、`daily`、`weekly`、`monthly` です。|
|runImmediatelyIfAfterStartDateTime|Boolean|True の場合は、StartDateTime が過去の場合はすぐにタスクを実行します。それ以外の場合は、次の定期的なパターンが実行されます。|

## <a name="relationships"></a>リレーションシップ
なし

## <a name="json-representation"></a>JSON 表記
以下は、リソースの JSON 表記です。
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10AppsForceUpdateSchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10AppsForceUpdateSchedule",
  "startDateTime": "String (timestamp)",
  "recurrence": "String",
  "runImmediatelyIfAfterStartDateTime": true
}
```



