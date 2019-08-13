---
title: defenderPotentiallyUnwantedAppAction 列挙型
description: 検出された望ましくない可能性があるアプリケーション (PUA) に対して実行する、Defender のアクション。
author: rolyon
localization_priority: Normal
ms.prod: Intune
doc_type: enumPageType
ms.openlocfilehash: 229b06fd2a4cfd525845fe1ff79cdd27b5fa01ab
ms.sourcegitcommit: b5425ebf648572569b032ded5b56e1dcf3830515
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "36333521"
---
# <a name="defenderpotentiallyunwantedappaction-enum-type"></a>defenderPotentiallyUnwantedAppAction 列挙型

> **重要:** ベータ版の Microsoft Graph Api は変更される可能性があります。運用環境での使用はサポートされていません。

> **注:** Microsoft Graph API for Intune では、テナントに対して[アクティブな intune ライセンス](https://go.microsoft.com/fwlink/?linkid=839381)が必要です。

検出された望ましくない可能性があるアプリケーション (PUA) に対して実行する、Defender のアクション。

## <a name="members"></a>メンバー
|メンバー|値|説明|
|:---|:---|:---|
|deviceDefault|.0|PUA の保護がオフになっています。 Defender は望ましくない可能性があるアプリケーションに対する保護を行いません。|
|拒否|1-d|PUA の保護がオンになっています。 検出されたアイテムはブロックされます。 これらのメンバーは、他の脅威と共に履歴に表示されます。|
|監査|pbm-2|監査モード。 Defender は望ましくない可能性があるアプリケーションを検出しますが、アクションは実行しません。 イベントビューアーで、Defender によって作成されたイベントを検索することによって、アプリケーション Defender が操作を実行したことについての情報を確認できます。|



