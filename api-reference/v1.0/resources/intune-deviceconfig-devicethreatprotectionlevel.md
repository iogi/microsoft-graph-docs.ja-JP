---
title: deviceThreatProtectionLevel 列挙型
description: デバイスの脅威保護 API のデバイスの脅威保護レベルです。
ms.openlocfilehash: 9b6a5066c26dcfe5ee2922bc736cf0292b1d3055
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/29/2018
ms.locfileid: "27023681"
---
# <a name="devicethreatprotectionlevel-enum-type"></a>deviceThreatProtectionLevel 列挙型

> **注:** Intune のコントロールおよびポリシーの構成に Microsoft Graph API を使用するには、これまでどおりに顧客が Intune サービスの[適切なライセンス](https://go.microsoft.com/fwlink/?linkid=839381)を持っている必要があります。

デバイスの脅威保護 API のデバイスの脅威保護レベルです。
## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|利用不可|0|既定値です。 使用しないでください。|
|セキュリティで保護|1|デバイスの脅威のレベルの要件: セキュリティで保護します。 これは、最も安全なレベルであり、デバイス上の脅威が見つかりませんだったことを表します。|
|低|2|デバイスの脅威保護に必要なレベル: 低。 低は、デバイスまたはデバイスのデータに最小限のリスクをもたらす脅威の重大度レベルを表します。|
|medium|3|デバイスの脅威保護に必要なレベル: 中。 [中] では、中程度のデバイスまたはデバイスのデータへのリスクをポーズする脅威の重大度レベルを表します。|
|高|4|デバイスの脅威保護に必要なレベル: 高。 高では、デバイスまたはデバイスのデータに重大なリスクをもたらす脅威の重大度レベルを表します。|
|notSet|10|デバイスの脅威保護に必要なレベル: 設定されていません。 セットはない、脅威保護のレベルを満たすためにデバイスの要件がないことです。|


