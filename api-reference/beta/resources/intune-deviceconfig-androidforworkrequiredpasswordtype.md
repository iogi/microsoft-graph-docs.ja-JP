---
title: androidForWorkRequiredPasswordType 列挙型
description: Android の作業には、パスワード入力が必要です。
ms.openlocfilehash: 8866ac49126f39204e0323082bf80e27f5f59962
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27069098"
---
# <a name="androidforworkrequiredpasswordtype-enum-type"></a>androidForWorkRequiredPasswordType 列挙型

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

Android の作業には、パスワード入力が必要です。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|0|デバイスの既定値でことを目的しません。|
|lowSecurityBiometric|1|低レベルのセキュリティ ベースの生体認証パスワードが必要です。|
|必須|2|必須。|
|atLeastNumeric|3|数値以上のパスワードが必要です。|
|numericComplex|4|数値の複雑なパスワードが必要です。|
|atLeastAlphabetic|5|少なくともアルファベットのパスワードが必要です。|
|atLeastAlphanumeric|6|以上の英数字のパスワードが必要です。|
|alphanumericWithSymbols|7|少なくとも文字の英数字の記号のパスワードが必要です。|




