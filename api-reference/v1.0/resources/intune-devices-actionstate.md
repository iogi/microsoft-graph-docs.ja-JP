---
title: actionState 列挙型
description: デバイス上のアクションの状態
ms.openlocfilehash: 1a18eb87cb4c9162777d16dc866de5f5766c87b1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27023732"
---
# <a name="actionstate-enum-type"></a>actionState 列挙型

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

デバイス上のアクションの状態
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|none|0|アクションが有効な状態ではなく|
|保留中|1|操作が保留中です。|
|キャンセル|2|アクションが取り消されました。|
|アクティブです|3|影響はありません。|
|done|4|操作がエラーなく完了しました。|
|失敗しました。|5|操作が失敗しました|
|notSupported|6|アクションはサポートされていません。|


