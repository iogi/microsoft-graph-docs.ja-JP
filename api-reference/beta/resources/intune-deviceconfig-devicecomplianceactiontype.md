---
title: deviceComplianceActionType 列挙型
description: 列挙型の操作をスケジュールします。
ms.openlocfilehash: 98e54f163663cc041a3e3c31123504c051884309
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27069539"
---
# <a name="devicecomplianceactiontype-enum-type"></a>deviceComplianceActionType 列挙型

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

列挙型の操作をスケジュールします。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|noAction|0|操作は必要ありません。|
|通知|1|通知を送信します。|
|ブロック|2|AAD でデバイスをブロックします。|
|退職|3|デバイスを破棄します。|
|ワイプ|4|デバイスをワイプします。|
|removeResourceAccessProfiles|5|デバイスからリソースのアクセス ・ プロファイルを削除します。|
|pushNotification|9|デバイスにプッシュ通知を送信します。|
|remoteLock|10|リモートでデバイスをロックします。|




