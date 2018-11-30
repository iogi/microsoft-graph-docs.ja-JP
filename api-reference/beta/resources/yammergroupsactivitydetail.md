---
title: yammerGroupsActivityDetail リソースの種類
description: リソースの JSON 表記を次に示します。
ms.openlocfilehash: 9a4bb00aecb2ae1d14b68a5388e0dedc7c41b1cb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27067444"
---
# <a name="yammergroupsactivitydetail-resource-type"></a>yammerGroupsActivityDetail リソースの種類

## <a name="properties"></a>プロパティ

| プロパティ           | 型    |
| :----------------- | :------ |
| reportRefreshDate  | Date    |
| groupDisplayName   | String  |
| isDeleted          | ブール値 |
| ownerPrincipalName | String  |
| lastActivityDate   | Date    |
| groupType          | String  |
| office365Connected | ブール値 |
| membercount プロパティ        | Int64   |
| postedCount        | Int64   |
| readCount          | Int64   |
| likedCount         | Int64   |
| reportPeriod       | String  |

## <a name="json-representation"></a>JSON 表記

リソースの JSON 表記を次に示します。

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerGroupsActivityDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "groupDisplayName": "String", 
  "isDeleted": true, 
  "ownerPrincipalName": "String", 
  "lastActivityDate": "Date", 
  "groupType": "String", 
  "office365Connected": true, 
  "memberCount": 1024, 
  "postedCount": 1024, 
  "readCount": 1024, 
  "likedCount": 1024, 
  "reportPeriod": "String"
}
```