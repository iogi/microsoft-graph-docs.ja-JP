---
title: androidDeviceOwnerSystemUpdateInstallType 列挙型
description: Android デバイスの所有者のシステム更新プログラムの種類。
ms.openlocfilehash: e9f23fd96ed0965b6693776858082e2df4925f37
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27070420"
---
# <a name="androiddeviceownersystemupdateinstalltype-enum-type"></a>androidDeviceOwnerSystemUpdateInstallType 列挙型

> **重要:** Microsoft Graph のベータ版 (/beta) の API はプレビュー中であるため、変更されることがあります。 実稼働アプリケーションでの、これらの API の使用はサポートされていません。

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

Android デバイスの所有者のシステム更新プログラムの種類。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|0|デバイス既定の動作、通常システムの更新を許可するユーザーを求められます。|
|延期|1|30 日以内に更新プログラムの自動インストールを延期します。|
|ウィンドウ表示|2|保守時間帯の毎日の中には、自動的にインストールします。|
|自動|3|できるだけ早く更新を自動的にインストールします。|




