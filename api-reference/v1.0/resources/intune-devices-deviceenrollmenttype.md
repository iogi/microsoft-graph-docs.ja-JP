---
title: deviceEnrollmentType 列挙型
description: 管理するモバイル デバイスを追加するための方法です。
ms.openlocfilehash: 5c921e30f642e1d44d675f8bee7a5b79c53ce428
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27020272"
---
# <a name="deviceenrollmenttype-enum-type"></a>deviceEnrollmentType 列挙型

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

管理するモバイル デバイスを追加するための方法です。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|不明|0|登録型の既定値は収集されませんでした。|
|userEnrollment|1|BYOD チャネルを通じてユーザー駆動の登録します。|
|deviceEnrollmentManager|2|デバイス登録の管理者アカウントとユーザー登録します。|
|appleBulkWithUser|3|アップル一括登録はユーザーの課題です。 (DEP、Apple の構成ウィザード)|
|appleBulkWithoutUser|4|ユーザーの課題に Apple の一括登録します。 (DEP では、Apple の構成ウィザードは、モバイルの設定)|
|windowsAzureADJoin|5|Windows Azure AD を 10 に参加します。|
|windowsBulkUserless|6|証明書で ICD を Windows 10 一括登録します。|
|windowsAutoEnrollment|7|10 の Windows の自動登録します。 (勤務先のアカウントを追加)|
|windowsBulkAzureDomainJoin|8|10 の windows Azure AD に参加を一括します。|
|windowsCoManagement|9|Windows 10 共同管理自動操縦装置、またはグループ ポリシーによって発生します。|


