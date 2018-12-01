---
title: deviceRegistrationState 列挙型
description: デバイス登録のステータス。
ms.openlocfilehash: 5496bce53e061894a829745fce0687815c855c01
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27073447"
---
# <a name="deviceregistrationstate-enum-type"></a>deviceRegistrationState 列挙型

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

デバイス登録のステータス。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|notRegistered|0|デバイスは登録されていません。|
|登録|2|デバイスが登録されています。|
|失効|3|デバイスがブロックされている、消去した廃止します。|
|keyConflict|4|デバイスには、キーの競合があります。|
|approvalPending|5|デバイスは、承認が保留中です。|
|certificateReset|6|デバイスの証明書をリセットするとします。|
|notRegisteredPendingEnrollment|7|デバイスが登録されていないと登録を保留中です。|
|不明|8|デバイス ライセンス登録のステータスは不明です。|




